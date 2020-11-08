---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106544"
---
# <span data-ttu-id="f2b3f-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="f2b3f-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="f2b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b3f-103">Sanal makinelerde kullanılabilen en son uzantılara yönelik bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="f2b3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2b3f-104">SYNTAX</span></span>

### <span data-ttu-id="f2b3f-105">ListLatestExtensions (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2b3f-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2b3f-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="f2b3f-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2b3f-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="f2b3f-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2b3f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2b3f-108">DESCRIPTION</span></span>
<span data-ttu-id="f2b3f-109">**Get-AzureVMAvailableExtension** cmdlet 'i sanal makinelerde kullanılabilir en son uzantılara yönelik bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="f2b3f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2b3f-110">EXAMPLES</span></span>

### <span data-ttu-id="f2b3f-111">Örnek 1: kullanılabilir en son uzantılar için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f2b3f-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="f2b3f-112">Bu komut, tüm sanal makinelerde kullanılabilen en son uzantılara yönelik bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="f2b3f-113">Örnek 2: belirtilen bir uzantı adından bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f2b3f-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="f2b3f-114">Bu komut, VMAccessAgent adındaki ve Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="f2b3f-115">Örnek 3: belirli bir sanal makine uzantısından sürüm numarasıyla bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f2b3f-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="f2b3f-116">Bu komut, VMAccessAgent adlı uzantıya ve Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="f2b3f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2b3f-117">PARAMETERS</span></span>

### <span data-ttu-id="f2b3f-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="f2b3f-118">-AllVersions</span></span>
<span data-ttu-id="f2b3f-119">Bu cmdlet 'in bir uzantının tüm sürümlerini listediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="f2b3f-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f2b3f-120">-ExtensionName</span></span>
<span data-ttu-id="f2b3f-121">Kullanılabilir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="f2b3f-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f2b3f-122">-InformationAction</span></span>
<span data-ttu-id="f2b3f-123">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2b3f-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f2b3f-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2b3f-125">'A</span><span class="sxs-lookup"><span data-stu-id="f2b3f-125">Continue</span></span>
- <span data-ttu-id="f2b3f-126">Manıza</span><span class="sxs-lookup"><span data-stu-id="f2b3f-126">Ignore</span></span>
- <span data-ttu-id="f2b3f-127">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f2b3f-127">Inquire</span></span>
- <span data-ttu-id="f2b3f-128">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f2b3f-128">SilentlyContinue</span></span>
- <span data-ttu-id="f2b3f-129">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f2b3f-129">Stop</span></span>
- <span data-ttu-id="f2b3f-130">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f2b3f-130">Suspend</span></span>

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

### <span data-ttu-id="f2b3f-131">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f2b3f-131">-InformationVariable</span></span>
<span data-ttu-id="f2b3f-132">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2b3f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2b3f-133">-Profile</span></span>
<span data-ttu-id="f2b3f-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2b3f-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2b3f-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f2b3f-136">-Publisher</span></span>
<span data-ttu-id="f2b3f-137">Uzantının yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="f2b3f-138">-Version</span><span class="sxs-lookup"><span data-stu-id="f2b3f-138">-Version</span></span>
<span data-ttu-id="f2b3f-139">Uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="f2b3f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b3f-140">CommonParameters</span></span>
<span data-ttu-id="f2b3f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2b3f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b3f-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b3f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b3f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2b3f-143">INPUTS</span></span>

## <span data-ttu-id="f2b3f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2b3f-144">OUTPUTS</span></span>

## <span data-ttu-id="f2b3f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2b3f-145">NOTES</span></span>

## <span data-ttu-id="f2b3f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2b3f-146">RELATED LINKS</span></span>

