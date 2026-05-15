# React Alert Component

A highly customizable, responsive, and beautiful alert component system for React applications. Built with TypeScript, Sass, and Lucide Icons.

![Alert Component Demo](https://raw.githubusercontent.com/AbanoubPhelopos/react-alert-project/main/public/demo.png)

## ✨ Features

- 🎨 **Multiple Variants**: Success, Error, Warning, Info, and Default styles.
- 🧩 **Flexible Content**: Support for both simple string descriptions and complex React children.
- 🛠️ **Fully Typed**: Built with TypeScript for excellent developer experience.
- ⚡ **Vite Powered**: Ultra-fast development and build process.
- 📦 **Lucide Icons**: Integrated with the beautiful Lucide icon library.
- 📱 **Responsive Design**: Looks great on all screen sizes.

## 🚀 Getting Started

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AbanoubPhelopos/react-alert-project.git
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```

## 🛠️ Usage

Import the `Alert` component and the desired icons:

```tsx
import { Bell, Info, CheckCheck, Ban, AlertTriangle } from "lucide-react";
import Alert from "./components/ui/Alert";

const App = () => {
  return (
    <div style={{ padding: "2rem" }}>
      {/* Default Alert with Children */}
      <Alert type="alert-default" icon={<Bell size={20} />} title="Upgrade your plan">
        <p>
          Enhance your experience by upgrading to a premium plan. <a href="/">Learn more</a>.
        </p>
      </Alert>

      {/* Info Alert with Description Prop */}
      <Alert
        type="alert-info"
        icon={<Info size={20} />}
        title="Note"
        description="This is a helpful information message for the user."
      />

      {/* Success Alert */}
      <Alert
        type="alert-success"
        icon={<CheckCheck size={20} />}
        title="Success"
        description="Your changes have been saved successfully!"
      />
    </div>
  );
};
```

## 📋 Props

The `Alert` component accepts the following props:

| Prop | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `type` | `AlertTypes` | `"alert-error"` | The visual style of the alert. |
| `icon` | `ReactNode` | **Required** | The icon to display in the header. |
| `title` | `string` | **Required** | The main heading text. |
| `description` | `string` | `undefined` | Simple text content for the alert. |
| `children` | `ReactNode` | `undefined` | Complex content (overrides `description` if provided). |

### AlertTypes
Available types:
- `"alert-default"`
- `"alert-info"`
- `"alert-success"`
- `"alert-error"`
- `"alert-warning"`

## 🎨 Customization

### Sass Variables
The component's theme can be easily customized by modifying the Sass variables in `src/components/ui/Alert/index.scss`:

| Variable | Description |
| :--- | :--- |
| `$defaultBg`, `$infoBg`, etc. | Background colors for each alert type. |
| `$defaultColor`, `$infoColor`, etc. | Text colors for each alert type. |
| `$defaultBorder`, `$infoBorder`, etc. | Border colors for each alert type. |

### Mixins
The styles are generated using a Sass mixin, making it easy to add new alert types if needed:

```scss
@include alert("alert-custom", $customBg, $customColor, $customBorder);
```

## 📄 License

This project is open-sourced under the MIT License. Created by [Abanoub Phelopos](https://github.com/AbanoubPhelopos).
