---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105606"
---
# <span data-ttu-id="8a0c5-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="8a0c5-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="8a0c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0c5-103">Barındırılan hizmetler için kullanılabilir uzantılar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="8a0c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a0c5-104">SYNTAX</span></span>

### <span data-ttu-id="8a0c5-105">ListLatestExtensions (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a0c5-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0c5-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="8a0c5-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a0c5-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="8a0c5-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a0c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a0c5-108">DESCRIPTION</span></span>
<span data-ttu-id="8a0c5-109">**Get-Azurezerviceavailableextension** cmdlet 'i barındırılan hizmetler için kullanılabilir en son uzantılara yönelik bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="8a0c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a0c5-110">EXAMPLES</span></span>

### <span data-ttu-id="8a0c5-111">Örnek 1: kullanılabilir uzantıları alma</span><span class="sxs-lookup"><span data-stu-id="8a0c5-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="8a0c5-112">Bu komut kullanılabilir tüm uzantıları alır.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="8a0c5-113">Örnek 2: belirtilen ad alanında uzantıları alma</span><span class="sxs-lookup"><span data-stu-id="8a0c5-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="8a0c5-114">Bu komut belirtilen ad alanında belirtilen ada sahip uzantıları alır.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="8a0c5-115">Örnek 3: uzantının belirli bir sürümünü alma</span><span class="sxs-lookup"><span data-stu-id="8a0c5-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="8a0c5-116">Bu komut, uzantının belirli bir sürümü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="8a0c5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a0c5-117">PARAMETERS</span></span>

### <span data-ttu-id="8a0c5-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="8a0c5-118">-AllVersions</span></span>
<span data-ttu-id="8a0c5-119">Bu cmdlet 'in bir uzantının tüm sürümlerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="8a0c5-120">-ExtensionName</span></span>
<span data-ttu-id="8a0c5-121">Uzantı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8a0c5-122">-InformationAction</span></span>
<span data-ttu-id="8a0c5-123">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a0c5-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a0c5-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a0c5-125">'A</span><span class="sxs-lookup"><span data-stu-id="8a0c5-125">Continue</span></span>
- <span data-ttu-id="8a0c5-126">Manıza</span><span class="sxs-lookup"><span data-stu-id="8a0c5-126">Ignore</span></span>
- <span data-ttu-id="8a0c5-127">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="8a0c5-127">Inquire</span></span>
- <span data-ttu-id="8a0c5-128">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="8a0c5-128">SilentlyContinue</span></span>
- <span data-ttu-id="8a0c5-129">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="8a0c5-129">Stop</span></span>
- <span data-ttu-id="8a0c5-130">Biliriz</span><span class="sxs-lookup"><span data-stu-id="8a0c5-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-131">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="8a0c5-131">-InformationVariable</span></span>
<span data-ttu-id="8a0c5-132">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="8a0c5-133">-Profile</span></span>
<span data-ttu-id="8a0c5-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a0c5-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="8a0c5-136">-ProviderNamespace</span></span>
<span data-ttu-id="8a0c5-137">Uzantı sağlayıcı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-138">-Version</span><span class="sxs-lookup"><span data-stu-id="8a0c5-138">-Version</span></span>
<span data-ttu-id="8a0c5-139">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a0c5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0c5-140">CommonParameters</span></span>
<span data-ttu-id="8a0c5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a0c5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0c5-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a0c5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0c5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a0c5-143">INPUTS</span></span>

## <span data-ttu-id="8a0c5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a0c5-144">OUTPUTS</span></span>

## <span data-ttu-id="8a0c5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a0c5-145">NOTES</span></span>

## <span data-ttu-id="8a0c5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a0c5-146">RELATED LINKS</span></span>

[<span data-ttu-id="8a0c5-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="8a0c5-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


