# Usability Principles for Complex 3D & CAD Interfaces

Derived from studies of parametric design tools, CAD systems, and professional 3D applications, plus established heuristics adapted for high-complexity domains.

## Core Principles

1. **Suitability for the task**  
   Every UI element should support efficient completion of real 3D design tasks. Avoid decorative or low-value chrome.

2. **Self-descriptiveness**  
   Icons, labels, and states must be immediately understandable. Use consistent visual language. Tooltips should include the action name + shortcut.

3. **Conformity with user expectations**  
   Match the interaction model of tools the target users already know. Deviating requires strong justification and excellent onboarding.

4. **Learnability & progressive disclosure**  
   Simple default path for beginners. Power features (customization, scripting, advanced panels) available but not forced.

5. **Controllability**  
   Users must feel in control of the viewport, selection, and history. Undo/redo must be robust and visible.

6. **Error tolerance**  
   Prevent invalid states where possible. Make recovery easy. Never lose work silently.

7. **User engagement & flow**  
   Keep the artist in a creative flow state. Minimize mode switches, dialog interruptions, and waiting.

## Additional Guidelines for 3D Tools

- **Visibility of system status**: Always show current mode, selection count, active tool, and whether the scene is dirty/saved.
- **Aesthetic and minimalist design (adapted)**: Remove unnecessary elements, but do not sacrifice density that experts need. Use visual hierarchy and grouping instead of pure minimalism.
- **Recognition rather than recall**: Keep frequently used tools and properties visible or one click away. Search as safety net.
- **Flexibility and efficiency of use**: Accelerators, customization, and scripting for experts; guided paths for novices.
- **Consistency and standards**: Same action = same result across the application. Follow platform and industry standards.
- **Help and documentation**: Contextual help, searchable manual, and tooltips that actually help.

## Performance & Responsiveness
- UI thread must never freeze during viewport redraws or heavy calculations.
- Provide progress feedback for long operations.
- Use progressive refinement, LODs, and background computation where appropriate.

## Accessibility Considerations
- High-contrast themes (many 3D artists work in dark environments).
- Scalable UI and font sizes.
- Full keyboard operability for non-viewport tasks.
- Clear focus indicators.
- Avoid relying solely on color to convey state.
