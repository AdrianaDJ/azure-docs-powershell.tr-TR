---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09300c7d7d8394dbcfed36560c988f0193473c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572562"
---
# <span data-ttu-id="8cb58-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="8cb58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cb58-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb58-103">Belirli bir coğrafi konumda Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cb58-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8cb58-104">SYNTAX</span></span>

### <span data-ttu-id="8cb58-105">S1</span><span class="sxs-lookup"><span data-stu-id="8cb58-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cb58-106">S2</span><span class="sxs-lookup"><span data-stu-id="8cb58-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cb58-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8cb58-107">DESCRIPTION</span></span>
<span data-ttu-id="8cb58-108">**Yeni-AzureRmAppServicePlan** cmdlet 'ı belirtilen katmana, çalışan boyutuna ve çalışan sayısına sahip belirli bir coğrafi konumda bir Azure App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cb58-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="8cb58-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8cb58-109">EXAMPLES</span></span>

### <span data-ttu-id="8cb58-110">Örnek 1: App Service planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8cb58-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="8cb58-111">Bu komut, coğrafi konum olarak varsayılan-Web-WestUS adlı kaynak grubunda ContosoASP adında bir App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cb58-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="8cb58-112">Komut temel bir katmanı belirtir ve iki küçük çalışanı ayırır.</span><span class="sxs-lookup"><span data-stu-id="8cb58-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="8cb58-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8cb58-113">PARAMETERS</span></span>

### <span data-ttu-id="8cb58-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-114">-AppServicePlan</span></span>
<span data-ttu-id="8cb58-115">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="8cb58-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb58-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="8cb58-116">-AseName</span></span>
<span data-ttu-id="8cb58-117">App Service ortamı adı</span><span class="sxs-lookup"><span data-stu-id="8cb58-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="8cb58-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb58-118">-AseResourceGroupName</span></span>
<span data-ttu-id="8cb58-119">App Service ortamı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8cb58-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="8cb58-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="8cb58-120">-AsJob</span></span>
<span data-ttu-id="8cb58-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8cb58-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb58-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb58-122">-DefaultProfile</span></span>
<span data-ttu-id="8cb58-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8cb58-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb58-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="8cb58-124">-HyperV</span></span>
<span data-ttu-id="8cb58-125">Bunu belirtin App Service planı Windows kapsayıcılarını çalıştırır</span><span class="sxs-lookup"><span data-stu-id="8cb58-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb58-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="8cb58-126">-Location</span></span>
<span data-ttu-id="8cb58-127">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="8cb58-127">Location</span></span> 

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

### <span data-ttu-id="8cb58-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="8cb58-128">-Name</span></span>
<span data-ttu-id="8cb58-129">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="8cb58-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="8cb58-130">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="8cb58-130">-NumberofWorkers</span></span>
<span data-ttu-id="8cb58-131">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="8cb58-131">Number Of Workers</span></span>

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

### <span data-ttu-id="8cb58-132">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="8cb58-132">-PerSiteScaling</span></span>
<span data-ttu-id="8cb58-133">Site Ölçeklendirmesi başına etkinleştirilip etkinleştirilmeyeceği</span><span class="sxs-lookup"><span data-stu-id="8cb58-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="8cb58-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb58-134">-ResourceGroupName</span></span>
<span data-ttu-id="8cb58-135">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8cb58-135">Resource Group Name</span></span>

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

### <span data-ttu-id="8cb58-136">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="8cb58-136">-Tier</span></span>
<span data-ttu-id="8cb58-137">Katman</span><span class="sxs-lookup"><span data-stu-id="8cb58-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb58-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="8cb58-138">-WorkerSize</span></span>
<span data-ttu-id="8cb58-139">Web çalışanı boyutu</span><span class="sxs-lookup"><span data-stu-id="8cb58-139">Size of web worker</span></span>

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

### <span data-ttu-id="8cb58-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb58-140">CommonParameters</span></span>
<span data-ttu-id="8cb58-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8cb58-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb58-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb58-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb58-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8cb58-143">INPUTS</span></span>

### <span data-ttu-id="8cb58-144">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-144">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="8cb58-145">Parametreler: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8cb58-145">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="8cb58-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8cb58-146">OUTPUTS</span></span>

### <span data-ttu-id="8cb58-147">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-147">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="8cb58-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8cb58-148">NOTES</span></span>

## <span data-ttu-id="8cb58-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8cb58-149">RELATED LINKS</span></span>

[<span data-ttu-id="8cb58-150">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-150">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="8cb58-151">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-151">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="8cb58-152">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cb58-152">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


