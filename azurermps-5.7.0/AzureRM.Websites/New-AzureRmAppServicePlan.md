---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09491e82a1eb0ab6b77a382fc727d385bbd6820f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763938"
---
# <span data-ttu-id="9ada6-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ada6-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9ada6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ada6-102">SYNOPSIS</span></span>
<span data-ttu-id="9ada6-103">Belirli bir coğrafi konumda Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ada6-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ada6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ada6-104">SYNTAX</span></span>

### <span data-ttu-id="9ada6-105">S1</span><span class="sxs-lookup"><span data-stu-id="9ada6-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ada6-106">S2</span><span class="sxs-lookup"><span data-stu-id="9ada6-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ada6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ada6-107">DESCRIPTION</span></span>
<span data-ttu-id="9ada6-108">**Yeni-AzureRmAppServicePlan** cmdlet 'ı belirtilen katmana, çalışan boyutuna ve çalışan sayısına sahip belirli bir coğrafi konumda bir Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ada6-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="9ada6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ada6-109">EXAMPLES</span></span>

### <span data-ttu-id="9ada6-110">Örnek 1: App Service planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ada6-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="9ada6-111">Bu komut, coğrafi konum olarak varsayılan-Web-WestUS adlı kaynak grubunda ContosoASP adında bir App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ada6-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="9ada6-112">Komut temel bir katmanı belirtir ve iki küçük çalışanı ayırır.</span><span class="sxs-lookup"><span data-stu-id="9ada6-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="9ada6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ada6-113">PARAMETERS</span></span>

### <span data-ttu-id="9ada6-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ada6-114">-AppServicePlan</span></span>
<span data-ttu-id="9ada6-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="9ada6-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="9ada6-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="9ada6-116">-AseName</span></span>
<span data-ttu-id="9ada6-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="9ada6-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="9ada6-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ada6-118">-AseResourceGroupName</span></span>
<span data-ttu-id="9ada6-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9ada6-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9ada6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ada6-120">-DefaultProfile</span></span>
<span data-ttu-id="9ada6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ada6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ada6-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="9ada6-122">-Location</span></span>
<span data-ttu-id="9ada6-123">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="9ada6-123">Location</span></span> 

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

### <span data-ttu-id="9ada6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ada6-124">-Name</span></span>
<span data-ttu-id="9ada6-125">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="9ada6-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="9ada6-126">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="9ada6-126">-NumberofWorkers</span></span>
<span data-ttu-id="9ada6-127">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="9ada6-127">Number Of Workers</span></span>

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

### <span data-ttu-id="9ada6-128">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="9ada6-128">-PerSiteScaling</span></span>
<span data-ttu-id="9ada6-129">Site Ölçeklendirmesi başına etkinleştirilip etkinleştirilmeyeceği</span><span class="sxs-lookup"><span data-stu-id="9ada6-129">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="9ada6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ada6-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ada6-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9ada6-131">Resource Group Name</span></span>

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

### <span data-ttu-id="9ada6-132">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="9ada6-132">-Tier</span></span>
<span data-ttu-id="9ada6-133">Katman</span><span class="sxs-lookup"><span data-stu-id="9ada6-133">Tier</span></span>

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

### <span data-ttu-id="9ada6-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="9ada6-134">-WorkerSize</span></span>
<span data-ttu-id="9ada6-135">Web çalışanı boyutu</span><span class="sxs-lookup"><span data-stu-id="9ada6-135">Size of web worker</span></span>

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
### <span data-ttu-id="9ada6-136">-Iş</span><span class="sxs-lookup"><span data-stu-id="9ada6-136">-AsJob</span></span>
<span data-ttu-id="9ada6-137">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9ada6-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ada6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ada6-138">CommonParameters</span></span>
<span data-ttu-id="9ada6-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ada6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ada6-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ada6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ada6-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ada6-141">INPUTS</span></span>

### <span data-ttu-id="9ada6-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9ada6-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="9ada6-143">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9ada6-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="9ada6-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ada6-144">OUTPUTS</span></span>

### <span data-ttu-id="9ada6-145">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9ada6-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="9ada6-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ada6-146">NOTES</span></span>

## <span data-ttu-id="9ada6-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ada6-147">RELATED LINKS</span></span>

[<span data-ttu-id="9ada6-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ada6-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="9ada6-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ada6-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="9ada6-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9ada6-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


