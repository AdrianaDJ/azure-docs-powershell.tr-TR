---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: 015a16ec40e7b5159e6082acd47f2583edff1f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939208"
---
# <span data-ttu-id="6fe18-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fe18-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="6fe18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe18-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe18-103">Belirli bir coğrafi konumda Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fe18-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fe18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fe18-104">SYNTAX</span></span>

### <span data-ttu-id="6fe18-105">S1</span><span class="sxs-lookup"><span data-stu-id="6fe18-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe18-106">S2</span><span class="sxs-lookup"><span data-stu-id="6fe18-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fe18-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fe18-107">DESCRIPTION</span></span>
<span data-ttu-id="6fe18-108">**Yeni-AzureRmAppServicePlan** cmdlet 'ı belirtilen katmana, çalışan boyutuna ve çalışan sayısına sahip belirli bir coğrafi konumda bir Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fe18-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="6fe18-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fe18-109">EXAMPLES</span></span>

### <span data-ttu-id="6fe18-110">Örnek 1: App Service planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6fe18-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="6fe18-111">Bu komut, coğrafi konum olarak varsayılan-Web-WestUS adlı kaynak grubunda ContosoASP adında bir App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fe18-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="6fe18-112">Komut temel bir katmanı belirtir ve iki küçük çalışanı ayırır.</span><span class="sxs-lookup"><span data-stu-id="6fe18-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="6fe18-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fe18-113">PARAMETERS</span></span>

### <span data-ttu-id="6fe18-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fe18-114">-AppServicePlan</span></span>
<span data-ttu-id="6fe18-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="6fe18-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="6fe18-116">-AseName</span></span>
<span data-ttu-id="6fe18-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="6fe18-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe18-118">-AseResourceGroupName</span></span>
<span data-ttu-id="6fe18-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6fe18-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe18-120">-DefaultProfile</span></span>
<span data-ttu-id="6fe18-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fe18-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="6fe18-122">-Location</span></span>
<span data-ttu-id="6fe18-123">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="6fe18-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fe18-124">-Name</span></span>
<span data-ttu-id="6fe18-125">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="6fe18-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-126">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="6fe18-126">-NumberofWorkers</span></span>
<span data-ttu-id="6fe18-127">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="6fe18-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-128">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="6fe18-128">-PerSiteScaling</span></span>
<span data-ttu-id="6fe18-129">Site Ölçeklendirmesi başına etkinleştirilip etkinleştirilmeyeceği</span><span class="sxs-lookup"><span data-stu-id="6fe18-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe18-130">-ResourceGroupName</span></span>
<span data-ttu-id="6fe18-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6fe18-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-132">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="6fe18-132">-Tier</span></span>
<span data-ttu-id="6fe18-133">Katman</span><span class="sxs-lookup"><span data-stu-id="6fe18-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe18-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="6fe18-134">-WorkerSize</span></span>
<span data-ttu-id="6fe18-135">Web çalışanı boyutu</span><span class="sxs-lookup"><span data-stu-id="6fe18-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="6fe18-136">-Iş</span><span class="sxs-lookup"><span data-stu-id="6fe18-136">-AsJob</span></span>
<span data-ttu-id="6fe18-137">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6fe18-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fe18-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe18-138">CommonParameters</span></span>
<span data-ttu-id="6fe18-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fe18-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe18-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe18-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe18-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fe18-141">INPUTS</span></span>

### <span data-ttu-id="6fe18-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6fe18-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="6fe18-143">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6fe18-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="6fe18-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fe18-144">OUTPUTS</span></span>

### <span data-ttu-id="6fe18-145">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6fe18-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="6fe18-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fe18-146">NOTES</span></span>

## <span data-ttu-id="6fe18-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fe18-147">RELATED LINKS</span></span>

[<span data-ttu-id="6fe18-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fe18-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="6fe18-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fe18-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="6fe18-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fe18-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)

