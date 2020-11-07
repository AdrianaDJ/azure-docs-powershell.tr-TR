---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764501"
---
# <span data-ttu-id="f625e-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f625e-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="f625e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f625e-102">SYNOPSIS</span></span>
<span data-ttu-id="f625e-103">Belirli bir coğrafi konumda Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f625e-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f625e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f625e-104">SYNTAX</span></span>

### <span data-ttu-id="f625e-105">S1</span><span class="sxs-lookup"><span data-stu-id="f625e-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f625e-106">S2</span><span class="sxs-lookup"><span data-stu-id="f625e-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f625e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f625e-107">DESCRIPTION</span></span>
<span data-ttu-id="f625e-108">**Yeni-AzureRmAppServicePlan** cmdlet 'ı belirtilen katmana, çalışan boyutuna ve çalışan sayısına sahip belirli bir coğrafi konumda bir Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f625e-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="f625e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f625e-109">EXAMPLES</span></span>

### <span data-ttu-id="f625e-110">Örnek 1: App Service planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f625e-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="f625e-111">Bu komut, coğrafi konum olarak varsayılan-Web-WestUS adlı kaynak grubunda ContosoASP adında bir App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f625e-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="f625e-112">Komut temel bir katmanı belirtir ve iki küçük çalışanı ayırır.</span><span class="sxs-lookup"><span data-stu-id="f625e-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="f625e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f625e-113">PARAMETERS</span></span>

### <span data-ttu-id="f625e-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f625e-114">-AppServicePlan</span></span>
<span data-ttu-id="f625e-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f625e-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="f625e-116">-AseName</span></span>
<span data-ttu-id="f625e-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="f625e-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f625e-118">-AseResourceGroupName</span></span>
<span data-ttu-id="f625e-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f625e-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="f625e-120">-Location</span></span>
<span data-ttu-id="f625e-121">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="f625e-121">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f625e-122">-Name</span></span>
<span data-ttu-id="f625e-123">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="f625e-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-124">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="f625e-124">-NumberofWorkers</span></span>
<span data-ttu-id="f625e-125">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="f625e-125">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-126">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="f625e-126">-PerSiteScaling</span></span>
<span data-ttu-id="f625e-127">Site Ölçeklendirmesi başına etkinleştirilip etkinleştirilmeyeceği</span><span class="sxs-lookup"><span data-stu-id="f625e-127">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f625e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f625e-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f625e-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-130">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="f625e-130">-Tier</span></span>
<span data-ttu-id="f625e-131">Katman</span><span class="sxs-lookup"><span data-stu-id="f625e-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="f625e-132">-WorkerSize</span></span>
<span data-ttu-id="f625e-133">Web çalışanı boyutu</span><span class="sxs-lookup"><span data-stu-id="f625e-133">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f625e-134">-DefaultProfile</span></span>
<span data-ttu-id="f625e-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f625e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f625e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f625e-136">CommonParameters</span></span>
<span data-ttu-id="f625e-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f625e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f625e-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f625e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f625e-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f625e-139">INPUTS</span></span>

### <span data-ttu-id="f625e-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="f625e-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="f625e-141">' AppServicePlan ' parametresi ardışık düzenin ' ServerFarmWithRichSku ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f625e-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="f625e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f625e-142">OUTPUTS</span></span>

### <span data-ttu-id="f625e-143">Microsoft. Azure. Management. Websiteleri. modeller. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="f625e-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="f625e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f625e-144">NOTES</span></span>

## <span data-ttu-id="f625e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f625e-145">RELATED LINKS</span></span>

[<span data-ttu-id="f625e-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f625e-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="f625e-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f625e-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="f625e-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f625e-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


