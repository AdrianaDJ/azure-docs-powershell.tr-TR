---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105607"
---
# <span data-ttu-id="1a30a-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1a30a-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="1a30a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a30a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a30a-103">Belirtilen dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Active Directory (AD) etki alanı uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="1a30a-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="1a30a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a30a-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a30a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a30a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a30a-106">**Get-AzureServiceADDomainExtension** cmdlet 'i belirtilen dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti ad etki alanı uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="1a30a-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="1a30a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a30a-107">EXAMPLES</span></span>

### <span data-ttu-id="1a30a-108">Örnek 1: belirtilen hizmet için AD etki alanı uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="1a30a-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="1a30a-109">Bu komut, $Svc belirtilen hizmetin AD etki alanı uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="1a30a-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="1a30a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a30a-110">PARAMETERS</span></span>

### <span data-ttu-id="1a30a-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1a30a-111">-InformationAction</span></span>
<span data-ttu-id="1a30a-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a30a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1a30a-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1a30a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a30a-114">'A</span><span class="sxs-lookup"><span data-stu-id="1a30a-114">Continue</span></span>
- <span data-ttu-id="1a30a-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="1a30a-115">Ignore</span></span>
- <span data-ttu-id="1a30a-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1a30a-116">Inquire</span></span>
- <span data-ttu-id="1a30a-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1a30a-117">SilentlyContinue</span></span>
- <span data-ttu-id="1a30a-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1a30a-118">Stop</span></span>
- <span data-ttu-id="1a30a-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1a30a-119">Suspend</span></span>

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

### <span data-ttu-id="1a30a-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1a30a-120">-InformationVariable</span></span>
<span data-ttu-id="1a30a-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a30a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1a30a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a30a-122">-Profile</span></span>
<span data-ttu-id="1a30a-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a30a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a30a-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1a30a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a30a-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="1a30a-125">-ServiceName</span></span>
<span data-ttu-id="1a30a-126">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a30a-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="1a30a-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1a30a-127">-Slot</span></span>
<span data-ttu-id="1a30a-128">Dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a30a-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="1a30a-129">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="1a30a-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="1a30a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a30a-130">CommonParameters</span></span>
<span data-ttu-id="1a30a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a30a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a30a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a30a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a30a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a30a-133">INPUTS</span></span>

## <span data-ttu-id="1a30a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a30a-134">OUTPUTS</span></span>

## <span data-ttu-id="1a30a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a30a-135">NOTES</span></span>

## <span data-ttu-id="1a30a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a30a-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a30a-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1a30a-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="1a30a-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1a30a-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


