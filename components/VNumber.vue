<template>
  <div class="number">
    <div class="line a" />
    <div class="group-line fb">
      <div class="line f" />
      <div class="line b" />
    </div>
    <div class="line g" />
    <div class="group-line ec">
      <div class="line e" />
      <div class="line c" />
    </div>
    <div class="line d" />
  </div>
</template>

<style lang="scss" scoped>

$shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
$radius: 5px;
@keyframes appear {
  0% {
    opacity: 0;
  }
}

.number {
  margin-right: 10px;
  color: white;

  &:nth-child(2n) {
    margin-right: 26px;
    position: relative;

    &:before, &:after {
      content: '';
      position: absolute;
      right: -17px;
      width: 4px;
      height: 4px;
    }

    &:before {
      top: 15px;
      border: dashed;
    }

    &:after {
      bottom: 15px;
      border: dashed;
    }
  }

  &:last-child {
    margin-right: 0;

    &:before, &:after {
      content: none;
    }
  }

  animation: 1s appear;
  width: 33px;
  height: 61px;

  &_1 {
    .a, .f, .g, .e, .d {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_2 {
    .f, .c {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_3 {
    .f, .e {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_4 {
    .a, .e, .d {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_5 {
    .b, .e {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_6 {
    .b {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_7 {
    .f, .g, .e, .d {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_8 {
    //
  }

  &_9 {
    .e {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }

  &_0 {
    .g {
      background: none;
      box-shadow: none;
      border: 0;
    }
  }
}

.line {
  box-shadow: $shadow;
}

.a, .g, .d {
  margin: 0 auto;
  width: 23px;
  height: 5px;
  border: dashed;
}

.b, .c, .e, .f {
  width: 5px;
  height: 23px;
  border: dashed;
}

.group-line {
  display: flex;
  justify-content: space-between;
}
</style>
