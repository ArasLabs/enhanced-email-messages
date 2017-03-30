# Federated Property for Enhancing Email Messages

The following two packages utilize a federated property of an ItemType to enhance what can be put into an email message. In both projects the hidden federated property is populated with data from one of the relationships.

The first project utilized an Item Comments thread to be included in an Email. The second project however adds details of an ECR or ECN affected items into the email message trigger by Activities.

It is sometimes necessary to have an Item that has a relationship to a comment thread. This comment thread allows users to add comments to an item regarding changes, instructions, or other information. However since these comments are part of relationship they can not be populated as part of the Email Message.

These email messages can be triggered as notifications of Workflows, on Life Cycle Promotions or even from within method code.

The following package which can be imported populates a federated property on the Parent Item with the comments from the relationship. Then when the item is promoted the Comments are sent as part of the email.

The second projects main goal is to add more details about the affected Item into the email message. The document outlines how to use a server method to populate a Federate property on either the ECR or ECN item type. This federated property will include the Affected items owned_by_id identity, the affected item Type, and a link to the Affected Item.

Please note an email Address must be associated with Innovator Admin for testing.

## History

This project and the following release notes have been migrated from the old Aras Projects page. Unlike community projects that have been migrated and archived, this project will be updated for compatibility with the latest release of Aras Innovator.

Release | Notes
--------|--------
[v2](https://github.com/ArasLabs/enhanced-email-messages/releases/tag/v2) | Federated Affected Item Details for Email Messages Document. Can be used in 9.1
[v1](https://github.com/ArasLabs/enhanced-email-messages/releases/tag/v1) | Federated Comments Package for Import for 9.0.1 and 9.0.2 only.

#### Supported Aras Versions

Project | Aras
--------|------
[v2](https://github.com/ArasLabs/enhanced-email-messages/releases/tag/v2) | 9.1, 9.2
[v1](https://github.com/ArasLabs/enhanced-email-messages/releases/tag/v1) | 9.0.1, 9.0.2

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed
2. Aras Package Import tool
3. **Federated_Comments** import packages

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\enhanced-email-messages\Import\imports.mf` file in the Manifest File field.
6. Select **Federated_Comments** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Usage

For more information on using this project in Aras 9.1, refer to [Aras Innovator-Affected Item Details in Email.doc](.\Documentation\Aras%20Innovator-Affected%20Item%20Details%20in%20Email.doc).

## Credits

Created by Aras Corporation Support.

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
