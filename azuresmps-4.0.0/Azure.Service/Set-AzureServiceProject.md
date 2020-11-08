---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105819"
---
# <span data-ttu-id="92e45-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="92e45-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="92e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e45-102">SYNOPSIS</span></span>
<span data-ttu-id="92e45-103">Geçerli hizmet için varsayılan konumu, aboneliği, yuvayı ve depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92e45-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="92e45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92e45-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="92e45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92e45-105">DESCRIPTION</span></span>
<span data-ttu-id="92e45-106">**Set-AzureServiceProject** cmdlet 'i geçerli hizmet için dağıtım konumunu, yuvayı, depolama hesabını ve aboneliği ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92e45-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="92e45-107">Bu değerler, hizmet bulutta yayımlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="92e45-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="92e45-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92e45-108">EXAMPLES</span></span>

### <span data-ttu-id="92e45-109">Örnek 1: temel ayarlar</span><span class="sxs-lookup"><span data-stu-id="92e45-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="92e45-110">Hizmetin dağıtım konumunu Kuzey Merkezi ABD bölgesine ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92e45-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="92e45-111">Dağıtım yuvasını üretime ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92e45-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="92e45-112">Hizmet tanımını myStorageAccount olarak hazırlamak için kullanılacak depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92e45-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="92e45-113">Hizmeti mySubscription 'a barındıracak aboneliği ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92e45-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="92e45-114">Hizmet buluta yayımlandığında, bu, Kuzey Merkezi ABD bölgesindeki bir veri merkezinde barındırılır, dağıtım yuvasını güncelleştirecek ve belirtilen aboneliği ve depolama hesabını kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="92e45-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="92e45-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92e45-115">PARAMETERS</span></span>

### <span data-ttu-id="92e45-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="92e45-116">-Location</span></span>
<span data-ttu-id="92e45-117">Hizmetin barındırıldığı bölge.</span><span class="sxs-lookup"><span data-stu-id="92e45-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="92e45-118">Hizmet buluta yayımlandığında bu değer kullanılır.</span><span class="sxs-lookup"><span data-stu-id="92e45-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="92e45-119">Olası değerler: tüm Asya, Avrupa, ABD, Doğu Asya, Doğu ABD, Kuzey Merkezi ABD, Kuzey Avrupa, Güney Merkez ABD, Güneydoğu Asya, Batı Avrupa, Batı ABD.</span><span class="sxs-lookup"><span data-stu-id="92e45-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

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

### <span data-ttu-id="92e45-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="92e45-120">-PassThru</span></span>
<span data-ttu-id="92e45-121">Bu cmdlet 'in, üzerinde işlem yaptığı öğeyi temsil eden bir nesne döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="92e45-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="92e45-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="92e45-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e45-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="92e45-123">-Profile</span></span>
<span data-ttu-id="92e45-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92e45-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92e45-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="92e45-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92e45-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="92e45-126">-Slot</span></span>
<span data-ttu-id="92e45-127">Hizmetin barındırıldığı yuva (üretim veya hazırlama).</span><span class="sxs-lookup"><span data-stu-id="92e45-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="92e45-128">Hizmet buluta yayımlandığında bu değer kullanılır.</span><span class="sxs-lookup"><span data-stu-id="92e45-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="92e45-129">Olası değerler: üretim, aşamalandırma.</span><span class="sxs-lookup"><span data-stu-id="92e45-129">Possible values are: Production, Staging.</span></span>

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

### <span data-ttu-id="92e45-130">-Depolama</span><span class="sxs-lookup"><span data-stu-id="92e45-130">-Storage</span></span>
<span data-ttu-id="92e45-131">Hizmet paketi buluta yüklenirken kullanılacak depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="92e45-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="92e45-132">Depolama hesabı yoksa, hizmet buluta yayımlandığında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="92e45-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

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

### <span data-ttu-id="92e45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e45-133">CommonParameters</span></span>
<span data-ttu-id="92e45-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92e45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e45-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e45-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e45-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92e45-136">INPUTS</span></span>

## <span data-ttu-id="92e45-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92e45-137">OUTPUTS</span></span>

## <span data-ttu-id="92e45-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92e45-138">NOTES</span></span>
* <span data-ttu-id="92e45-139">düğüm-dev, php-dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="92e45-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="92e45-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92e45-140">RELATED LINKS</span></span>

[<span data-ttu-id="92e45-141">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="92e45-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="92e45-142">Yayımla-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="92e45-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="92e45-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="92e45-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


