---
title: Perceivable
slug: Web/Accessibility/Guides/Understanding_WCAG/Perceivable
page-type: guide
sidebar: accessibilitysidebar
---

This article provides practical advice on how to write your web content so that it conforms to the success criteria outlined in the **Perceivable** principle of the Web Content Accessibility Guidelines (WCAG) 2.0 and 2.1. Perceivable states that users must be able to perceive it in some way, using one or more of their senses.

> [!NOTE]
> To read the W3C definitions for Perceivable and its guidelines and success criteria, see [Principle 1: Perceivable - Information and user interface components must be presentable to users in ways they can perceive.](https://w3c.github.io/wcag/guidelines/22/#perceivable)

## Guideline 1.1 — Providing text alternatives for non-text content

The key here is that text can be converted to other forms that people with disabilities can use. For example, it can be spoken by a screen reader, converted to large print, or represented on a braille display. Non-text content refers to multimedia such as images, audio, and video.

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col">Success criteria</th>
      <th scope="col">How to conform to the criteria</th>
      <th scope="col">Practical resource</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="5">1.1.1 Provide text equivalents (A)</td>
      <td>
        All images that convey meaningful content should be given suitable
        alternative text.
      </td>
      <td>
        <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML#text_alternatives"
          >Text alternatives.</a
        >
      </td>
    </tr>
    <tr>
      <td>
        Complex images or charts should have an accessible alternative provided,
        either on the same page or via a link. Use a regular link instead of
        a <code>longdesc</code> attribute.
      </td>
      <td>
        <p>
          A text description may work, or an accessible data table (see
          <a href="/en-US/docs/Learn_web_development/Core/Structuring_content/Table_accessibility"
            >HTML table accessibility</a
          >). See W3C's
          <a href="https://www.w3.org/TR/html-longdesc/">Image Description Extension (longdesc)</a>
          for the argument against <code>longdesc</code>.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        Multimedia content (i.e., audio or video) should at least have a
        descriptive identification available, such as a caption or similar.
      </td>
      <td>
        <p>
          See <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML#text_alternatives"
            >Text alternatives</a
          >
          for static caption options, and
          <a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#audio_transcripts"
            >Audio transcripts</a
          >,
          <a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#video_text_tracks"
            >Video text tracks</a
          >
          for other alternatives.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        UI controls such as form elements and buttons should have text labels
        that describe their purpose.
      </td>
      <td>
        Buttons are simple—you should make sure the button text describes the
        function of the button (e.g., <code
          >&#x3C;button>Upload image&#x3C;/button></code
        >). For more information on other UI controls, see
        <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML#use_semantic_ui_controls_where_possible"
          >Use semantic UI controls where possible</a
        >.
      </td>
    </tr>
    <tr>
      <td>
        Implement decorative (non-content) images, video, etc., in a way that is
        invisible to assistive technology, so it doesn't confuse users.
      </td>
      <td>
        <p>
          Decorative images should be implemented using CSS background images
          (see
          <a
            href="/en-US/docs/Learn_web_development/Core/Styling_basics/Backgrounds_and_borders"
            >Backgrounds and borders</a
          >). If you have to include an image via an
          {{htmlelement("img")}} element, give it a blank alt
          (<code>alt=""</code>). Otherwise, screen readers may try to read out
          the filepath, etc.
        </p>
        <p>
          If you are including background video or audio that autoplays, make it
          as unobtrusive as possible. Don't make it look/sound like content, and
          provide a control to turn it off. Ideally, don't include it at all.
        </p>
      </td>
    </tr>
  </tbody>
</table>

> [!NOTE]
> Also see the [WCAG description for Guideline 1.1: Text alternatives](https://w3c.github.io/wcag/guidelines/22/#text-alternatives).

## Guideline 1.2 — Providing text alternatives for time-based media

Time-based media refers to multimedia with a duration, such as audio and video. Note that if the audio/video serves as an alternative to existing text content, you don't need to provide another text alternative.

<table>
  <thead>
    <tr>
       <th scope="col">Success criteria</th>
       <th scope="col">How to conform to the criteria</th>
       <th scope="col">Practical resource</th>
    </tr>
  </thead>
  <tbody>
    <tr>
       <td>1.2.1 Provide alternatives for pre-recorded audio-only and video-only content (A)</td>
       <td>A transcript should be provided for prerecorded audio-only media, and a transcript or audio description should be provided for prerecorded video-only media (i.e., silent video).</td>
       <td>See&nbsp;<a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#audio_transcripts">Audio transcripts</a> for transcript information. No audio description tutorial is available yet.</td>
    </tr>
    <tr>
       <td>1.2.2 Provide captions for web-based video (A)</td>
       <td>You should provide captions for video presented on the web (e.g., HTML video). This is for the benefit of people who can't hear the audio part of the video.</td>
       <td>See <a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#video_text_tracks">Video text tracks</a> for HTML video captions. See also <a href="https://support.google.com/youtube/answer/2734796?hl=en">Add your own subtitles &amp; closed captions</a> (YouTube).</td>
    </tr>
    <tr>
       <td>1.2.3 Provide text transcript or audio description for web-based video (A)</td>
       <td>You should provide text transcripts or audio descriptions for video presented on the web (e.g., HTML video. This is for the benefit of people who can't see the visual part of the video, and don't get the full content from the audio alone.</td>
       <td>See&nbsp;<a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#audio_transcripts">Audio transcripts</a> for transcript information. No audio description tutorial is available yet.</td>
    </tr>
    <tr>
       <td>1.2.4 Provide captions for live audio (AA)</td>
       <td>You should provide synchronized captions for all live multimedia that contains audio (e.g., video conferences, live audio broadcasts).</td>
       <td></td>
    </tr>
    <tr>
       <td>1.2.5 Provide audio descriptions for prerecorded video (AA)</td>
       <td>Audio descriptions should be provided for prerecorded video, but only where the existing audio does not convey the full meaning expressed by the video.</td>
       <td></td>
    </tr>
    <tr>
       <td>1.2.6 Provide sign language equivalent to prerecorded audio (AAA)</td>
       <td>An equivalent sign language video should be provided for any prerecorded content containing audio.</td>
       <td></td>
    </tr>
    <tr>
       <td>1.2.7 Provide extended video with audio descriptions (AAA)</td>
       <td>Where audio descriptions cannot be provided (see 1.2.5) due to video timing issues (e.g., there are no suitable pauses in the content in which to insert the audio descriptions), an alternative version of the video should be provided that includes inserted pauses (and audio descriptions).</td>
       <td></td>
    </tr>
    <tr>
       <td>1.2.8 Provide an alternative for prerecorded media (AAA)</td>
       <td>For all content that features video, a descriptive text transcript should be provided, for example a script of the movie you are watching. This is for the benefit of hearing-impaired viewers who cannot hear the content.</td>
       <td>See&nbsp;<a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#audio_transcripts">Audio transcripts</a> for transcript information.</td>
    </tr>
    <tr>
       <td>1.2.9 Provide a transcript for live audio (AAA)</td>
       <td>For any live audio content being broadcast, a descriptive text should be provided, for example a script of the play or musical you are listening to. This is for the benefit of hearing-impaired viewers who cannot hear the content.</td>
       <td>See&nbsp;<a href="/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia#audio_transcripts">Audio transcripts</a> for transcript information.</td>
    </tr>
 </tbody>
</table>

> [!NOTE]
> Also see the [WCAG description for Guideline 1.2: Time-based Media: Provide alternatives for time-based media](https://w3c.github.io/wcag/guidelines/22/#time-based-media).

## Guideline 1.3 — Create content that can be presented in different ways

This guideline refers to the ability of content to be consumed by users in multiple ways, accommodating their differing needs.

<table class="standard-table">
  <tbody>
    <tr>
      <th scope="col">Success criteria</th>
      <th scope="col">How to conform to the criteria</th>
      <th scope="col">Practical resource</th>
    </tr>
    <tr>
      <td>1.3.1 Info and relationships (A)</td>
      <td>
        <p>
          Any content structure—or visual relationship made between content—can
          also be determined programmatically, or be inferred from text
          description. The main situations in which this is relevant are:
        </p>
        <ul>
          <li>
            Text labels and the form elements they describe. These are
            associated unambiguously using the {{htmlelement("label")}}
            element, which can be picked up by screen readers, etc.
          </li>
          <li>
            Image alt text. Content images should have text available that
            clearly describes the image's contents, which can be
            programmatically associated with it (e.g., alt text),
            or otherwise is easy to associate (e.g., describes it and is sat
            right next to it). This should mean that the full meaning can still
            be inferred even if you can't see the image.
          </li>
          <li>
            Lists. If the order of list items is important, use an ordered list
            ({{htmlelement("ol")}}).
          </li>
        </ul>
      </td>
      <td>
        The whole of
        <p>
          <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML"
            >HTML: A good basis for accessibility</a
          >
          is packed with information about this, but you should particularly
          refer to
          <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML#good_semantics"
            >Good semantics</a
          >,
          <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML#use_semantic_ui_controls_where_possible"
            >Use semantic UI controls where possible</a
          >, and
          <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML#text_alternatives"
            >Text alternatives</a
          >.
        </p>
      </td>
    </tr>
    <tr>
      <td>1.3.2 Meaningful content sequence (A)</td>
      <td>
        A sensible, logical reading order should be easy to determine for any
        content, even if it is visually presented in an unusual way. The order
        should be made obvious by use of correct semantic elements (e.g.,
        headings, paragraphs), with CSS being used to create any unusual layout
        styles, irrespective of the markup.
      </td>
      <td>
        Again, refer to
        <a href="/en-US/docs/Learn_web_development/Core/Accessibility/HTML"
          >HTML: A good basis for accessibility</a
        >.
      </td>
    </tr>
    <tr>
      <td>1.3.3 Sensory characteristics (A)</td>
      <td>
        <p>
          Instructions for operating controls or understanding content do not
          rely on a single sense. This may prove inaccessible to people with a
          disability related to that sense, or a device that does not support
          that sense. So, for example:
        </p>
        <ul>
          <li>
            "Click the round button to continue"<br />The button should be
            clearly labelled so that it is obvious that it is the button you
            need to press. If there are multiple buttons, make sure they are all
            clearly labelled to distinguish their function.
          </li>
          <li>
            "Listen to the audio instructions for guidance"<br />This is
            obviously problematic—audio will be inaccessible to those with
            hearing impairments, whereas text can be read, but also spoken by a
            screen reader if required.
          </li>
          <li>
            "Swipe from the right-hand side of the screen to reveal the menu"<br />Some
            users might not be able to swipe the screen, either due to
            disability or because their device does not support touch. An
            alternative should be provided, such as a keyboard shortcut or
            button that can be activated by keyboard or other means.
          </li>
        </ul>
        <div class="note notecard">
          <p>
            <strong>Note:</strong> Conveying instructions solely by color is
            related, but covered in a different guideline — 1.4.1.
          </p>
        </div>
      </td>
      <td></td>
    </tr>
    <tr>
      <td>
        1.3.4 Orientation (AA)
      </td>
      <td>
        Content does not restrict its view and operation to a single display
        orientation, such as portrait or landscape, unless a specific display
        orientation is essential.
      </td>
      <td>
        <p>
          <a href="https://www.w3.org/WAI/WCAG21/Understanding/orientation.html"
            >Understanding Orientation</a
          >
        </p>
      </td>
    </tr>
    <tr>
      <td>
        1.3.5 Identify Input Purpose (AA)
      </td>
      <td>
        <p>
          Follow the list of
          <a href="https://w3c.github.io/wcag/guidelines/22/#input-purposes"
            >53 input fields</a
          >
          to programmatically identify the purpose of a field.
        </p>
      </td>
      <td>
        <a
          href="https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html"
          >Understanding Identify Input Purpose</a
        >
      </td>
    </tr>
    <tr>
      <td>
        1.3.6 Identify Purpose (AAA)
      </td>
      <td>
        In content implemented using markup languages, the purpose of user
        interface components, icons, and regions can be programmatically
        determined.
      </td>
      <td>
        <a
          href="https://www.w3.org/WAI/WCAG21/Understanding/identify-purpose.html"
          >Understanding Identify Purpose</a
        >
      </td>
    </tr>
  </tbody>
</table>

> [!NOTE]
> Also see the WCAG description for [Guideline 1.3: Adaptable: Create content that can be presented in different ways without losing information or structure.](https://w3c.github.io/wcag/guidelines/22/#adaptable)

## Guideline 1.4: Make it easier for users to see and hear content including separating foreground from background

This guideline relates to making sure core content is easy to discern from backgrounds and other decoration. The classic example is color (both [color contrast](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Perceivable/Color_contrast) and [use of color](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Perceivable/Use_of_color) to convey instructions), but it applies in other situations too.

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col">Success criteria</th>
      <th scope="col">How to conform to the criteria</th>
      <th scope="col">Practical resource</th>
    </tr>
    <tr>
      <td>1.4.1 Use of color (A)</td>
      <td>
        <p>
          Color should not be solely relied upon to convey information. For
          example, in forms, you should never mark required fields purely with a
          color (like red). Instead (or as well as), something like an asterisk
          with a label of "required" would be more appropriate.
        </p>
      </td>
      <td>
        See
        <a href="/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Perceivable/Use_of_color"
          >Use of color</a
        >,
        <a
          href="/en-US/docs/Learn_web_development/Core/Accessibility/CSS_and_JavaScript#color_and_color_contrast"
          >Color and color contrast</a
        >,
        and
        <a
          href="/en-US/docs/Learn_web_development/Extensions/Forms/How_to_structure_a_web_form#multiple_labels"
          >Multiple labels</a
        >.
      </td>
    </tr>
    <tr>
      <td>1.4.2 Audio controls (A)</td>
      <td>
        For any audio that plays for longer than three seconds, provide
        accessible controls to play and pause the audio/video, and mute/adjust
        volume.
      </td>
      <td>
        Use native <code>&lt;button&gt;</code>s to provide accessible keyboard
        controls, as shown in
        <a
          href="/en-US/docs/Web/Media/Guides/Audio_and_video_delivery/Video_player_styling_basics"
          >Video player styling basics</a
        >.
      </td>
    </tr>
    <tr>
      <td>1.4.3 Minimum contrast (AA)</td>
      <td>
        <p>
          The color contrast between background and foreground content should be
          at a minimum level to ensure legibility:
        </p>
        <ul>
          <li>
            Text and its background should have a contrast ratio of at least
            4.5:1.
          </li>
          <li>
            Heading (or just larger) text should have a ratio of at least 3:1.
            Larger text is defined as at least 18pt, or 14pt bold.
          </li>
        </ul>
      </td>
      <td>
        See
        <a href="/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Perceivable/Color_contrast"
          >Color contrast</a
        > and
        <a
          href="/en-US/docs/Learn_web_development/Core/Accessibility/CSS_and_JavaScript#color_and_color_contrast"
          >Color and color contrast</a
        >.
      </td>
    </tr>
    <tr>
      <td>1.4.4 Resize text (AA)</td>
      <td>
        The page should be readable and usable when the text size is doubled.
        This means that designs should be responsive, so that when the text size
        is increased, the content is still accessible.
      </td>
      <td></td>
    </tr>
    <tr>
      <td>1.4.5 Images of text (AA)</td>
      <td>
        Images should NOT be used to present content where text would do the
        job. For example, if an image is mostly textual, it could be represented
        using text as well as images.
      </td>
      <td></td>
    </tr>
    <tr>
      <td>1.4.6 Enhanced contrast (AAA)</td>
      <td>
        <p>This follows, and builds on, criterion 1.4.3.</p>
        <ul>
          <li>
            Text and its background should have a contrast ratio of at least
            7:1.
          </li>
          <li>
            Heading (or just larger) text should have a ratio of at least 4.5:1.
            Larger text is defined as at least 18pt, or 14pt bold.
          </li>
        </ul>
      </td>
      <td>
        See
        <a
          href="/en-US/docs/Learn_web_development/Core/Accessibility/CSS_and_JavaScript#color_and_color_contrast"
          >Color and color contrast</a
        >.
      </td>
    </tr>
    <tr>
      <td>1.4.7 Low or no background audio (AAA)</td>
      <td>
        Prerecorded audio recordings that primarily feature speech should have
        minimal background noise, so the content can be easily understood.
      </td>
      <td></td>
    </tr>
    <tr>
      <td>1.4.8 Visual presentation (AAA)</td>
      <td>
        <p>For text content presentation, the following should be true:</p>
        <ul>
          <li>Foreground and background colors should be user-selectable.</li>
          <li>
            Text blocks should be no wider than 80 characters (or glyphs), for
            maximum readability.
          </li>
          <li>
            Text should not be fully justified (e.g., <code
              >text-align: justify;</code
            >).
          </li>
          <li>
            Line height should be at least 1.5 times the text size within
            paragraphs (e.g., <code>line-height: 1.5;</code>), and at least 2.25
            times the text size between paragraphs (e.g., <code
              >padding: 2.25rem;</code
            >).
          </li>
          <li>
            When the text size is doubled, the content should not need to be
            scrolled.
          </li>
        </ul>
      </td>
      <td></td>
    </tr>
    <tr>
      <td>1.4.9 Images of text (No Exception) (AAA)</td>
      <td>
        Text should not be presented as part of an image unless it is purely
        decoration (i.e., it does not convey any content) or cannot be presented
        in any other way.
      </td>
      <td></td>
    </tr>
    <tr>
      <td>
        1.4.10 Reflow (AA)
      </td>
      <td>
        <ul>
          <li>
            No horizontal scrolling for left-to-right languages (like English)
            or right-to-left languages (like Arabic)
          </li>
          <li>
            No vertical scrolling for top-to-bottom languages (like Japanese)
          </li>
          <li>
            Except for parts of the content which require two-dimensional layout
            for usage or meaning (like a large data table)
          </li>
        </ul>
      </td>
      <td>
        <a href="https://www.w3.org/WAI/WCAG21/Understanding/reflow.html"
          >Understanding Reflow</a
        >
      </td>
    </tr>
    <tr>
      <td>
        1.4.11 Non-Text Contrast(AA)
      </td>
      <td>
        Minimum color contrast ratio of 3:1 for user interface components and
        graphical objects.
      </td>
      <td>
        <a
          href="https://www.w3.org/WAI/WCAG21/Understanding/non-text-contrast.html"
          >Understanding Non-Text Contrast</a
        >
      </td>
    </tr>
    <tr>
      <td>
        1.4.12 Text Spacing (AA)
      </td>
      <td>
        <p>
          No loss of content or functionality occurs when the following styles
          are applied:
        </p>
        <ul>
          <li>
            Line height (line spacing) to at least 1.5 times the font size
          </li>
          <li>
            Spacing following paragraphs to at least 2 times the font size
          </li>
          <li>
            Letter spacing (tracking) to at least 0.12 times the font size
          </li>
          <li>Word spacing to at least 0.16 times the font size</li>
        </ul>
      </td>
      <td>
        <a href="https://www.w3.org/WAI/WCAG21/Understanding/text-spacing.html"
          >Understanding Text Spacing</a
        >
      </td>
    </tr>
    <tr>
      <td>
        1.4.13 Content on Hover or Focus (AA)
      </td>
      <td>
        <p>
          While additional content may appear and disappear in coordination with
          hover and keyboard focus, this success criterion specifies three
          conditions that must be met:
        </p>
        <ul>
          <li>dismissible (can be closed/removed)</li>
          <li>
            hoverable (the additional content does not disappear when the
            pointer is over it)
          </li>
          <li>
            persistent (the additional content does not disappear without user
            action)
          </li>
        </ul>
      </td>
      <td>
        <a
          href="https://www.w3.org/WAI/WCAG21/Understanding/content-on-hover-or-focus.html"
          >Understanding Content on Hover or Focus</a
        >
      </td>
    </tr>
  </thead>
</table>

> [!NOTE]
> Also see the WCAG description for [Guideline 1.4: Distinguishable: Make it easier for users to see and hear content including separating foreground from background.](https://w3c.github.io/wcag/guidelines/22/#distinguishable)

## See also

- [WCAG](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG)
  1. Perceivable
  2. [Operable](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Operable)
  3. [Understandable](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Understandable)
  4. [Robust](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Robust)
