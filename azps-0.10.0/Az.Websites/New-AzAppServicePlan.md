---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 040efd4e483825db637345fbd8bcb54a27e8675b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936099"
---
# <span data-ttu-id="7c775-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7c775-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="7c775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c775-102">SYNOPSIS</span></span>
<span data-ttu-id="7c775-103">Belirli bir coğrafi konumda Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c775-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="7c775-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c775-104">SYNTAX</span></span>

### <span data-ttu-id="7c775-105">S1</span><span class="sxs-lookup"><span data-stu-id="7c775-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c775-106">S2</span><span class="sxs-lookup"><span data-stu-id="7c775-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c775-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c775-107">DESCRIPTION</span></span>
<span data-ttu-id="7c775-108">**New-AzAppServicePlan** cmdlet 'ı belirtilen katmana, çalışan boyutuna ve çalışan sayısına sahip belirli bir coğrafi konumda bir Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c775-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="7c775-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c775-109">EXAMPLES</span></span>

### <span data-ttu-id="7c775-110">Örnek 1: App Service planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7c775-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="7c775-111">Bu komut, coğrafi konum olarak varsayılan-Web-WestUS adlı kaynak grubunda ContosoASP adında bir App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c775-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="7c775-112">Komut temel bir katmanı belirtir ve iki küçük çalışanı ayırır.</span><span class="sxs-lookup"><span data-stu-id="7c775-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="7c775-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c775-113">PARAMETERS</span></span>

### <span data-ttu-id="7c775-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7c775-114">-AppServicePlan</span></span>
<span data-ttu-id="7c775-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c775-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="7c775-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="7c775-116">-AseName</span></span>
<span data-ttu-id="7c775-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="7c775-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="7c775-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c775-118">-AseResourceGroupName</span></span>
<span data-ttu-id="7c775-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7c775-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="7c775-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c775-120">-DefaultProfile</span></span>
<span data-ttu-id="7c775-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c775-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c775-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="7c775-122">-Location</span></span>
<span data-ttu-id="7c775-123">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="7c775-123">Location</span></span> 

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

### <span data-ttu-id="7c775-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c775-124">-Name</span></span>
<span data-ttu-id="7c775-125">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="7c775-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="7c775-126">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="7c775-126">-NumberofWorkers</span></span>
<span data-ttu-id="7c775-127">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="7c775-127">Number Of Workers</span></span>

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

### <span data-ttu-id="7c775-128">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="7c775-128">-PerSiteScaling</span></span>
<span data-ttu-id="7c775-129">Site Ölçeklendirmesi başına etkinleştirilip etkinleştirilmeyeceği</span><span class="sxs-lookup"><span data-stu-id="7c775-129">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="7c775-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c775-130">-ResourceGroupName</span></span>
<span data-ttu-id="7c775-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7c775-131">Resource Group Name</span></span>

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

### <span data-ttu-id="7c775-132">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="7c775-132">-Tier</span></span>
<span data-ttu-id="7c775-133">Katman</span><span class="sxs-lookup"><span data-stu-id="7c775-133">Tier</span></span>

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

### <span data-ttu-id="7c775-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="7c775-134">-WorkerSize</span></span>
<span data-ttu-id="7c775-135">Web çalışanı boyutu</span><span class="sxs-lookup"><span data-stu-id="7c775-135">Size of web worker</span></span>

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
### <span data-ttu-id="7c775-136">-Iş</span><span class="sxs-lookup"><span data-stu-id="7c775-136">-AsJob</span></span>
<span data-ttu-id="7c775-137">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7c775-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c775-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c775-138">CommonParameters</span></span>
<span data-ttu-id="7c775-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c775-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c775-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c775-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c775-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c775-141">INPUTS</span></span>

### <span data-ttu-id="7c775-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7c775-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="7c775-143">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7c775-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="7c775-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c775-144">OUTPUTS</span></span>

### <span data-ttu-id="7c775-145">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7c775-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="7c775-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c775-146">NOTES</span></span>

## <span data-ttu-id="7c775-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c775-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c775-148">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7c775-148">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="7c775-149">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7c775-149">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="7c775-150">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7c775-150">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


