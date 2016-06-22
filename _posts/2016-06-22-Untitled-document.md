---
title: Mood Swing
layout: post
author: harry.keyland
permalink: /untitled-document/
source-id: 1OVzYexRLDtNvq6AQgi5WnGyDnyCBmAVeaGiB1AhXpT0
published: true
---
**Mood Swing**

/* When the BBC micro:bit runs   */

function onStart(  ) {

	while (true) {

		

		if (microbit.tiltY == 2) {

			

			microbit.draw(Pattern("01010.01010.00000.00000.11111"));

			

		}

		

		if (microbit.tiltY < 2) {

			

			microbit.draw(Pattern("01010.01010.00000.01110.10001"));

			

		}

		

		if (microbit.tiltY > 2) {

			

			microbit.draw(Pattern("01010.01010.00000.10001.01110"));

			

		}

