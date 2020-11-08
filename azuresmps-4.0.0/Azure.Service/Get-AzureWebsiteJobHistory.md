---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106507"
---
# <span data-ttu-id="aaadc-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="aaadc-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="aaadc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaadc-102">SYNOPSIS</span></span>
<span data-ttu-id="aaadc-103">Bir Web işi geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="aaadc-103">Gets a web job history.</span></span>

## <span data-ttu-id="aaadc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aaadc-104">SYNTAX</span></span>

### <span data-ttu-id="aaadc-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aaadc-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="aaadc-106">Runıdparametersetname</span><span class="sxs-lookup"><span data-stu-id="aaadc-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aaadc-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aaadc-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aaadc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aaadc-108">DESCRIPTION</span></span>
<span data-ttu-id="aaadc-109">Bir Web işi geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="aaadc-109">Gets a web job history.</span></span>

## <span data-ttu-id="aaadc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aaadc-110">EXAMPLES</span></span>

### <span data-ttu-id="aaadc-111">Örnek 1: Web işi için eksiksiz geçmişi alma</span><span class="sxs-lookup"><span data-stu-id="aaadc-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="aaadc-112">MyWebJob 'un tam geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="aaadc-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="aaadc-113">Örnek 2: Web işi için en son çalıştırmayı alma</span><span class="sxs-lookup"><span data-stu-id="aaadc-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="aaadc-114">MyWebJob için en son çalışma bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="aaadc-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="aaadc-115">Örnek 3: Web işi için belirli bir çalışma alma</span><span class="sxs-lookup"><span data-stu-id="aaadc-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="aaadc-116">MyWebJob için ID 10 ile çalışma hakkında tüm bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="aaadc-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="aaadc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aaadc-117">PARAMETERS</span></span>

### <span data-ttu-id="aaadc-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="aaadc-118">-JobName</span></span>
<span data-ttu-id="aaadc-119">Web işi adı.</span><span class="sxs-lookup"><span data-stu-id="aaadc-119">The web job name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaadc-120">-En son</span><span class="sxs-lookup"><span data-stu-id="aaadc-120">-Latest</span></span>
<span data-ttu-id="aaadc-121">Belirtilmişse, en son çalışma geçmişini döndürün.</span><span class="sxs-lookup"><span data-stu-id="aaadc-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadc-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="aaadc-122">-Name</span></span>
<span data-ttu-id="aaadc-123">Azure Web sitesinin adı.</span><span class="sxs-lookup"><span data-stu-id="aaadc-123">The name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaadc-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="aaadc-124">-Profile</span></span>
<span data-ttu-id="aaadc-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aaadc-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aaadc-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="aaadc-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aaadc-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="aaadc-127">-RunId</span></span>
<span data-ttu-id="aaadc-128">Görmek istediğiniz çalışma geçmişinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aaadc-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaadc-129">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="aaadc-129">-Slot</span></span>
<span data-ttu-id="aaadc-130">Azure Web sitesinin yuva adı.</span><span class="sxs-lookup"><span data-stu-id="aaadc-130">The slot name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaadc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaadc-131">CommonParameters</span></span>
<span data-ttu-id="aaadc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aaadc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaadc-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaadc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaadc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aaadc-134">INPUTS</span></span>

## <span data-ttu-id="aaadc-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aaadc-135">OUTPUTS</span></span>

## <span data-ttu-id="aaadc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aaadc-136">NOTES</span></span>

## <span data-ttu-id="aaadc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aaadc-137">RELATED LINKS</span></span>

[<span data-ttu-id="aaadc-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="aaadc-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="aaadc-139">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="aaadc-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="aaadc-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aaadc-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="aaadc-141">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aaadc-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="aaadc-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aaadc-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


