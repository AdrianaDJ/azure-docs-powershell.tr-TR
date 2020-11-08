---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105599"
---
# <span data-ttu-id="18114-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="18114-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="18114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18114-102">SYNOPSIS</span></span>
<span data-ttu-id="18114-103">Dağıtıma uygulanan bulut hizmeti uzantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="18114-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="18114-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18114-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="18114-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18114-105">DESCRIPTION</span></span>
<span data-ttu-id="18114-106">**Get-AzureServiceExtension** cmdlet 'i, dağıtıma uygulanan mevcut bulut hizmeti uzantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="18114-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="18114-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18114-107">EXAMPLES</span></span>

### <span data-ttu-id="18114-108">Örnek 1: Belirtilen uzantıyı alma</span><span class="sxs-lookup"><span data-stu-id="18114-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="18114-109">Bu komut, bulut hizmeti uzantısını belirtilen ad ve ad alanıyla alır.</span><span class="sxs-lookup"><span data-stu-id="18114-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="18114-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18114-110">PARAMETERS</span></span>

### <span data-ttu-id="18114-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="18114-111">-ExtensionName</span></span>
<span data-ttu-id="18114-112">Uzantı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18114-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="18114-113">-InformationAction</span></span>
<span data-ttu-id="18114-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="18114-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18114-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18114-116">'A</span><span class="sxs-lookup"><span data-stu-id="18114-116">Continue</span></span>
- <span data-ttu-id="18114-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="18114-117">Ignore</span></span>
- <span data-ttu-id="18114-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="18114-118">Inquire</span></span>
- <span data-ttu-id="18114-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="18114-119">SilentlyContinue</span></span>
- <span data-ttu-id="18114-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="18114-120">Stop</span></span>
- <span data-ttu-id="18114-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="18114-121">Suspend</span></span>

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

### <span data-ttu-id="18114-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="18114-122">-InformationVariable</span></span>
<span data-ttu-id="18114-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="18114-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="18114-124">-Profile</span></span>
<span data-ttu-id="18114-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18114-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="18114-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18114-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="18114-127">-ProviderNamespace</span></span>
<span data-ttu-id="18114-128">Uzantı sağlayıcı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18114-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="18114-129">-ServiceName</span></span>
<span data-ttu-id="18114-130">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-130">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18114-131">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="18114-131">-Slot</span></span>
<span data-ttu-id="18114-132">Dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18114-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="18114-133">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="18114-133">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18114-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18114-134">CommonParameters</span></span>
<span data-ttu-id="18114-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18114-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18114-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18114-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18114-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18114-137">INPUTS</span></span>

## <span data-ttu-id="18114-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18114-138">OUTPUTS</span></span>

## <span data-ttu-id="18114-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18114-139">NOTES</span></span>

## <span data-ttu-id="18114-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18114-140">RELATED LINKS</span></span>

[<span data-ttu-id="18114-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="18114-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="18114-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="18114-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


