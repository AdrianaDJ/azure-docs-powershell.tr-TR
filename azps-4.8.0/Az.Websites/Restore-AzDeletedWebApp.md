---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267916"
---
# <span data-ttu-id="a9b6c-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a9b6c-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="a9b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b6c-103">Silinmiş bir Web uygulamasını yeni veya varolan bir Web uygulamasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="a9b6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9b6c-104">SYNTAX</span></span>

### <span data-ttu-id="a9b6c-105">FromDeletedResourceName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9b6c-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b6c-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="a9b6c-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9b6c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="a9b6c-108">**Restore-AzDeletedWebApp** cmdlet 'i silinmiş bir Web uygulamasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="a9b6c-109">TargetResourceGroupName, hedefadı ve TargetSlot tarafından belirtilen Web uygulamasının üzerine, silinen Web uygulamasının içeriği ve ayarları yazılır.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="a9b6c-110">Hedef parametreler belirtilmemişse, otomatik olarak silinen Web uygulamasının kaynak grubu, adı ve yuvasına göre doldurulur.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="a9b6c-111">Hedef Web uygulaması yoksa, TargetAppServicePlanName tarafından belirtilen App Service planında otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="a9b6c-112">RestoreContentOnly Switch parametresi, uygulama ayarları olmadan yalnızca silinen uygulamanın dosyalarını geri yüklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="a9b6c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9b6c-113">EXAMPLES</span></span>

### <span data-ttu-id="a9b6c-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9b6c-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="a9b6c-115">Varsayılan-Web-WestUS kaynak grubuna ait olan ContosoApp adlı silinmiş bir uygulamayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="a9b6c-116">ContosoPlan adlı App Service planında aynı ada sahip ve kaynak grubuyla yeni bir uygulama oluşturulur ve silinen uygulamanın dosyaları ve ayarları bu dosyaya geri yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="a9b6c-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a9b6c-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="a9b6c-118">Varsayılan-Web-WestUS kaynak grubuna ait olan ContosoApp adlı silinen uygulamanın hazırlama yuvasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="a9b6c-119">Varsayılan-Web-EastUS kaynak grubuna ait olan ContosoRestore adlı Web uygulamasının üzerine yazılacak.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="a9b6c-120">Silinmiş Web App ayarları geri yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="a9b6c-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a9b6c-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="a9b6c-122">Aynı ada sahip 2 silinmiş uygulama (ContosoApp) olduğu durumlarda, hem sitelerin ayrıntılarını alır, hem de geri yükleme adlı uygulamayı seçmemiz için,</span><span class="sxs-lookup"><span data-stu-id="a9b6c-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="a9b6c-123">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a9b6c-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="a9b6c-124">Aynı ada sahip 2 silinmiş uygulama (ContosoApp) varsa, hem sitelerin ayrıntılarını alır, hem de geri yükle adlı uygulamayı, InputObject (Deletedsite) bilgileriyle geri yükleme</span><span class="sxs-lookup"><span data-stu-id="a9b6c-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="a9b6c-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9b6c-125">PARAMETERS</span></span>

### <span data-ttu-id="a9b6c-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="a9b6c-126">-AsJob</span></span>
<span data-ttu-id="a9b6c-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a9b6c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9b6c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b6c-128">-DefaultProfile</span></span>
<span data-ttu-id="a9b6c-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b6c-130">-Deletegerçekleşti</span><span class="sxs-lookup"><span data-stu-id="a9b6c-130">-DeletedId</span></span>
<span data-ttu-id="a9b6c-131">Silinen Azure Web uygulamasının kimliği.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-131">The Id of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="a9b6c-132">-Force</span></span>
<span data-ttu-id="a9b6c-133">Geri yüklemeyi, onay istemeden yapın.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a9b6c-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9b6c-134">-InputObject</span></span>
<span data-ttu-id="a9b6c-135">Silinen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-135">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="a9b6c-136">-Location</span></span>
<span data-ttu-id="a9b6c-137">Silinmiş Azure Web uygulamasının konumu.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-137">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9b6c-138">-Name</span></span>
<span data-ttu-id="a9b6c-139">Silinmiş Azure Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-139">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b6c-140">-ResourceGroupName</span></span>
<span data-ttu-id="a9b6c-141">Silinen Azure Web App 'in kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-141">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="a9b6c-142">-RestoreContentOnly</span></span>
<span data-ttu-id="a9b6c-143">Web uygulamasının dosyalarını geri yükleyin, ancak ayarları geri yüklemeyin.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="a9b6c-144">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a9b6c-144">-Slot</span></span>
<span data-ttu-id="a9b6c-145">Silinen Azure Web App yuvası.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-145">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="a9b6c-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="a9b6c-147">Yeni Azure Web App 'in App Service planı.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-147">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-148">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="a9b6c-148">-TargetName</span></span>
<span data-ttu-id="a9b6c-149">Yeni Azure Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-149">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b6c-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="a9b6c-151">Yeni Azure Web uygulamasını içeren kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-151">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="a9b6c-152">-TargetSlot</span></span>
<span data-ttu-id="a9b6c-153">Yeni Azure Web App yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-153">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-154">-Usedeyıldız</span><span class="sxs-lookup"><span data-stu-id="a9b6c-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="a9b6c-155">Silinen bir uygulamayı çevrimdışı olan bir ölçeklendirme biriminden kurtarmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="a9b6c-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9b6c-156">-Confirm</span></span>
<span data-ttu-id="a9b6c-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b6c-158">-WhatIf</span></span>
<span data-ttu-id="a9b6c-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9b6c-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9b6c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b6c-161">CommonParameters</span></span>
<span data-ttu-id="a9b6c-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9b6c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b6c-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b6c-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b6c-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9b6c-164">INPUTS</span></span>

### <span data-ttu-id="a9b6c-165">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a9b6c-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="a9b6c-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9b6c-166">OUTPUTS</span></span>

### <span data-ttu-id="a9b6c-167">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="a9b6c-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a9b6c-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9b6c-168">NOTES</span></span>

## <span data-ttu-id="a9b6c-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9b6c-169">RELATED LINKS</span></span>

[<span data-ttu-id="a9b6c-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a9b6c-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)