<svelte:head>
  <script src="./libs/html2canvas.min.js">

  </script>
  <script>
    function _toConsumableArray(t) {
      return (
        _arrayWithoutHoles(t) ||
        _iterableToArray(t) ||
        _unsupportedIterableToArray(t) ||
        _nonIterableSpread()
      );
    }
    function _nonIterableSpread() {
      throw new TypeError(
        "Invalid attempt to spread non-iterable instance.\nIn order to be iterable, non-array objects must have a [Symbol.iterator]() method."
      );
    }
    function _unsupportedIterableToArray(t, r) {
      if (t) {
        if ("string" == typeof t) return _arrayLikeToArray(t, r);
        var e = Object.prototype.toString.call(t).slice(8, -1);
        return (
          "Object" === e && t.constructor && (e = t.constructor.name),
          "Map" === e || "Set" === e
            ? Array.from(t)
            : "Arguments" === e ||
              /^(?:Ui|I)nt(?:8|16|32)(?:Clamped)?Array$/.test(e)
            ? _arrayLikeToArray(t, r)
            : void 0
        );
      }
    }
    function _iterableToArray(t) {
      if ("undefined" != typeof Symbol && Symbol.iterator in Object(t))
        return Array.from(t);
    }
    function _arrayWithoutHoles(t) {
      if (Array.isArray(t)) return _arrayLikeToArray(t);
    }
    function _arrayLikeToArray(t, r) {
      (null == r || r > t.length) && (r = t.length);
      for (var e = 0, a = new Array(r); e < r; e++) a[e] = t[e];
      return a;
    }
    var REPETITION_COUNT = 2,
      NUM_FRAMES = 21;
    function generateFrames(t) {
      for (
        var r =
            arguments.length > 1 && void 0 !== arguments[1]
              ? arguments[1]
              : NUM_FRAMES,
          e = t.width,
          a = t.height,
          n = t.getContext("2d"),
          o = n.getImageData(0, 0, e, a),
          i = _toConsumableArray(Array(r)).map(function (t, r) {
            return n.createImageData(e, a);
          }),
          c = 0;
        c < e;
        ++c
      )
        for (var l = 0; l < a; ++l)
          for (var s = 0; s < REPETITION_COUNT; ++s)
            for (
              var f = Math.floor((r * (Math.random() + (2 * c) / e)) / 3),
                y = 4 * (l * e + c),
                u = 0;
              u < 4;
              ++u
            )
              i[f].data[y + u] = o.data[y + u];
      return i.map(function (r) {
        var e = t.cloneNode(!0);
        return e.getContext("2d").putImageData(r, 0, 0), e;
      });
    }
    function replaceElementVisually(t, r) {
      var e = t.offsetParent;
      (r.style.top = "".concat(t.offsetTop, "px")),
        (r.style.left = "".concat(t.offsetLeft, "px")),
        (r.style.width = "".concat(t.offsetWidth, "px")),
        (r.style.height = "".concat(t.offsetHeight, "px")),
        e.appendChild(r),
        (t.style.visibility = "hidden");
    }
    function disintegrate(t) {
      html2canvas(t).then(function (r) {
        var e = document.createElement("div");
        e.classList.add("thanos-container");
        var a = generateFrames(r, NUM_FRAMES);
        a.forEach(function (t, r) {
          (t.style.transitionDelay = "".concat((1.13 * r) / a.length, "s")),
            e.appendChild(t);
        }),
          replaceElementVisually(t, e),
          e.offsetLeft,
          a.forEach(function (t) {
            (t.style.transform = "rotate("
              .concat(13 * (Math.random() - 0.55), "deg) translate(")
              .concat(55 * Math.cos(-1), "px, ")
              .concat(34 * Math.sin(-1), "px)\nrotate(")
              .concat(13 * (Math.random() - 0.55), "deg)")),
              (t.style.opacity = 0);
          });
      });
    }
  </script>
</svelte:head>
