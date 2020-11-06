---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590771"
---
# <span data-ttu-id="2f70b-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f70b-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2f70b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f70b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f70b-103">Bir Azure App Service planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2f70b-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f70b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f70b-104">SYNTAX</span></span>

### <span data-ttu-id="2f70b-105">S1</span><span class="sxs-lookup"><span data-stu-id="2f70b-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f70b-106">S2</span><span class="sxs-lookup"><span data-stu-id="2f70b-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f70b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f70b-107">DESCRIPTION</span></span>
<span data-ttu-id="2f70b-108">**Set-AzureRmAppServicePlan** cmdlet 'ı bir Azure App hizmet planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2f70b-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="2f70b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f70b-109">EXAMPLES</span></span>

### <span data-ttu-id="2f70b-110">1: App Service planını değiştirme</span><span class="sxs-lookup"><span data-stu-id="2f70b-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="2f70b-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı App Service planındaki Persiteölçeklendirme seçeneğini true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2f70b-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2f70b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f70b-112">PARAMETERS</span></span>

### <span data-ttu-id="2f70b-113">-Adminsiteadı</span><span class="sxs-lookup"><span data-stu-id="2f70b-113">-AdminSiteName</span></span>
<span data-ttu-id="2f70b-114">Yönetici sitesi adı</span><span class="sxs-lookup"><span data-stu-id="2f70b-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f70b-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f70b-115">-AppServicePlan</span></span>
<span data-ttu-id="2f70b-116">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="2f70b-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="2f70b-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="2f70b-117">-AsJob</span></span>
<span data-ttu-id="2f70b-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2f70b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f70b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f70b-119">-DefaultProfile</span></span>
<span data-ttu-id="2f70b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f70b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f70b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f70b-121">-Name</span></span>
<span data-ttu-id="2f70b-122">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="2f70b-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="2f70b-123">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="2f70b-123">-NumberofWorkers</span></span>
<span data-ttu-id="2f70b-124">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="2f70b-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f70b-125">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="2f70b-125">-PerSiteScaling</span></span>
<span data-ttu-id="2f70b-126">Site başına ölçeklendirme Boole değeri</span><span class="sxs-lookup"><span data-stu-id="2f70b-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f70b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f70b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f70b-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2f70b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="2f70b-129">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="2f70b-129">-Tier</span></span>
<span data-ttu-id="2f70b-130">Katman</span><span class="sxs-lookup"><span data-stu-id="2f70b-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f70b-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="2f70b-131">-WorkerSize</span></span>
<span data-ttu-id="2f70b-132">Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="2f70b-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f70b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f70b-133">CommonParameters</span></span>
<span data-ttu-id="2f70b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f70b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f70b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f70b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f70b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f70b-136">INPUTS</span></span>

### <span data-ttu-id="2f70b-137">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f70b-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="2f70b-138">Parametreler: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f70b-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="2f70b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f70b-139">OUTPUTS</span></span>

### <span data-ttu-id="2f70b-140">Microsoft. Azure. Management. Web sitesi. modeller. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f70b-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="2f70b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f70b-141">NOTES</span></span>

## <span data-ttu-id="2f70b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f70b-142">RELATED LINKS</span></span>

[<span data-ttu-id="2f70b-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2f70b-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2f70b-144">Yeni-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2f70b-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2f70b-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2f70b-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2f70b-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2f70b-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2f70b-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2f70b-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="2f70b-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2f70b-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


