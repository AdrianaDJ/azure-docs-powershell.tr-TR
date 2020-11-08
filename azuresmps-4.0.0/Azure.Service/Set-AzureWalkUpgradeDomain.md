---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105786"
---
# <span data-ttu-id="e1bed-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="e1bed-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="e1bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bed-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bed-103">Belirtilen yükseltme etki alanını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e1bed-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="e1bed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1bed-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1bed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1bed-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bed-106">**Set-AzureWalkUpgradeDomain** cmdlet 'ı bir Azure dağıtımının gerçek yükseltmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="e1bed-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="e1bed-107">Yükseltme paketi ve yapılandırması,-Upgrade anahtarı ile **set-AzureDeployment** cmdlet 'i kullanılarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e1bed-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="e1bed-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1bed-108">EXAMPLES</span></span>

### <span data-ttu-id="e1bed-109">Örnek 1: üretim dağıtımının yükseltmesini başlatma</span><span class="sxs-lookup"><span data-stu-id="e1bed-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="e1bed-110">Bu komut, MySvc1 hizmetinin üretim dağıtımının yükseltme etki alanı 2 yükseltmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="e1bed-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="e1bed-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1bed-111">PARAMETERS</span></span>

### <span data-ttu-id="e1bed-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="e1bed-112">-DomainNumber</span></span>
<span data-ttu-id="e1bed-113">Yükseltilecek yükseltme etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1bed-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bed-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e1bed-114">-InformationAction</span></span>
<span data-ttu-id="e1bed-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1bed-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e1bed-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e1bed-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1bed-117">'A</span><span class="sxs-lookup"><span data-stu-id="e1bed-117">Continue</span></span>
- <span data-ttu-id="e1bed-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="e1bed-118">Ignore</span></span>
- <span data-ttu-id="e1bed-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e1bed-119">Inquire</span></span>
- <span data-ttu-id="e1bed-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e1bed-120">SilentlyContinue</span></span>
- <span data-ttu-id="e1bed-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e1bed-121">Stop</span></span>
- <span data-ttu-id="e1bed-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e1bed-122">Suspend</span></span>

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

### <span data-ttu-id="e1bed-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e1bed-123">-InformationVariable</span></span>
<span data-ttu-id="e1bed-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1bed-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e1bed-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1bed-125">-Profile</span></span>
<span data-ttu-id="e1bed-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1bed-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1bed-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e1bed-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1bed-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e1bed-128">-ServiceName</span></span>
<span data-ttu-id="e1bed-129">Yükseltilecek Microsoft Azure hizmeti adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1bed-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bed-130">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="e1bed-130">-Slot</span></span>
<span data-ttu-id="e1bed-131">Yükseltilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1bed-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="e1bed-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e1bed-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1bed-133">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="e1bed-133">Staging</span></span>
- <span data-ttu-id="e1bed-134">Üretim</span><span class="sxs-lookup"><span data-stu-id="e1bed-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bed-135">CommonParameters</span></span>
<span data-ttu-id="e1bed-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1bed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bed-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bed-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bed-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1bed-138">INPUTS</span></span>

## <span data-ttu-id="e1bed-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1bed-139">OUTPUTS</span></span>

### <span data-ttu-id="e1bed-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e1bed-140">ManagementOperationContext</span></span>

## <span data-ttu-id="e1bed-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1bed-141">NOTES</span></span>

## <span data-ttu-id="e1bed-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1bed-142">RELATED LINKS</span></span>

[<span data-ttu-id="e1bed-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e1bed-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


