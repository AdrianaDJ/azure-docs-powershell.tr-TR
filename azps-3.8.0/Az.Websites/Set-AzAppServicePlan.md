---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: e33e80207b6490ef7197754af8857b2359e01400
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098378"
---
# <span data-ttu-id="a3a93-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3a93-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="a3a93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a93-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a93-103">Bir Azure App Service planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a3a93-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a3a93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3a93-104">SYNTAX</span></span>

### <span data-ttu-id="a3a93-105">S1</span><span class="sxs-lookup"><span data-stu-id="a3a93-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3a93-106">S2</span><span class="sxs-lookup"><span data-stu-id="a3a93-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a93-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3a93-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a93-108">**Set-AzAppServicePlan** cmdlet 'ı bir Azure App hizmet planı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a3a93-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a3a93-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3a93-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a93-110">1: App Service planını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a3a93-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="a3a93-111">Bu komut, Default-Web-WestUS adlı kaynak grubuna ait olan ContosoASP adlı App Service planındaki Persiteölçeklendirme seçeneğini true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a3a93-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a3a93-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3a93-112">PARAMETERS</span></span>

### <span data-ttu-id="a3a93-113">-Adminsiteadı</span><span class="sxs-lookup"><span data-stu-id="a3a93-113">-AdminSiteName</span></span>
<span data-ttu-id="a3a93-114">Yönetici sitesi adı</span><span class="sxs-lookup"><span data-stu-id="a3a93-114">Admin Site Name</span></span>

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

### <span data-ttu-id="a3a93-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3a93-115">-AppServicePlan</span></span>
<span data-ttu-id="a3a93-116">App Service planı nesnesi</span><span class="sxs-lookup"><span data-stu-id="a3a93-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="a3a93-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="a3a93-117">-AsJob</span></span>
<span data-ttu-id="a3a93-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a3a93-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3a93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a93-119">-DefaultProfile</span></span>
<span data-ttu-id="a3a93-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3a93-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a93-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3a93-121">-Name</span></span>
<span data-ttu-id="a3a93-122">App Service planı adı</span><span class="sxs-lookup"><span data-stu-id="a3a93-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="a3a93-123">-Işçilere</span><span class="sxs-lookup"><span data-stu-id="a3a93-123">-NumberofWorkers</span></span>
<span data-ttu-id="a3a93-124">Çalışan sayısı</span><span class="sxs-lookup"><span data-stu-id="a3a93-124">Number Of Workers</span></span>

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

### <span data-ttu-id="a3a93-125">-Persiteölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="a3a93-125">-PerSiteScaling</span></span>
<span data-ttu-id="a3a93-126">Site başına ölçeklendirme Boole değeri</span><span class="sxs-lookup"><span data-stu-id="a3a93-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="a3a93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a93-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3a93-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a3a93-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a3a93-129">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="a3a93-129">-Tier</span></span>
<span data-ttu-id="a3a93-130">Katman</span><span class="sxs-lookup"><span data-stu-id="a3a93-130">Tier</span></span>

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

### <span data-ttu-id="a3a93-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="a3a93-131">-WorkerSize</span></span>
<span data-ttu-id="a3a93-132">Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="a3a93-132">Worker Size</span></span>

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

### <span data-ttu-id="a3a93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a93-133">CommonParameters</span></span>
<span data-ttu-id="a3a93-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3a93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a93-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a93-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a93-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3a93-136">INPUTS</span></span>

### <span data-ttu-id="a3a93-137">Microsoft. Azure. Commands. WebApps. modeller. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3a93-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a3a93-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3a93-138">OUTPUTS</span></span>

### <span data-ttu-id="a3a93-139">Microsoft. Azure. Commands. WebApps. modeller. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a3a93-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a3a93-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3a93-140">NOTES</span></span>

## <span data-ttu-id="a3a93-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3a93-141">RELATED LINKS</span></span>

[<span data-ttu-id="a3a93-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a93-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a3a93-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a93-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a3a93-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a93-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a3a93-145">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a93-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a3a93-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a93-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="a3a93-147">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a3a93-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


