---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753782"
---
# <span data-ttu-id="d5242-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d5242-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="d5242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5242-102">SYNOPSIS</span></span>
<span data-ttu-id="d5242-103">Silinmiş bir Web uygulamasını yeni veya varolan bir Web uygulamasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="d5242-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="d5242-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5242-104">SYNTAX</span></span>

### <span data-ttu-id="d5242-105">FromDeletedResourceName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5242-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5242-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="d5242-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5242-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5242-107">DESCRIPTION</span></span>
<span data-ttu-id="d5242-108">**Restore-AzDeletedWebApp** cmdlet 'i silinmiş bir Web uygulamasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="d5242-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="d5242-109">TargetResourceGroupName, hedefadı ve TargetSlot tarafından belirtilen Web uygulamasının üzerine, silinen Web uygulamasının içeriği ve ayarları yazılır.</span><span class="sxs-lookup"><span data-stu-id="d5242-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="d5242-110">Hedef parametreler belirtilmemişse, otomatik olarak silinen Web uygulamasının kaynak grubu, adı ve yuvasına göre doldurulur.</span><span class="sxs-lookup"><span data-stu-id="d5242-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="d5242-111">Hedef Web uygulaması yoksa, TargetAppServicePlanName tarafından belirtilen App Service planında otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d5242-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="d5242-112">RestoreContentOnly Switch parametresi, uygulama ayarları olmadan yalnızca silinen uygulamanın dosyalarını geri yüklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d5242-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="d5242-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5242-113">EXAMPLES</span></span>

### <span data-ttu-id="d5242-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5242-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="d5242-115">Varsayılan-Web-WestUS kaynak grubuna ait olan ContosoApp adlı silinmiş bir uygulamayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="d5242-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d5242-116">ContosoPlan adlı App Service planında aynı ada sahip ve kaynak grubuyla yeni bir uygulama oluşturulur ve silinen uygulamanın dosyaları ve ayarları bu dosyaya geri yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="d5242-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="d5242-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d5242-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="d5242-118">Varsayılan-Web-WestUS kaynak grubuna ait olan ContosoApp adlı silinen uygulamanın hazırlama yuvasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="d5242-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d5242-119">Varsayılan-Web-EastUS kaynak grubuna ait olan ContosoRestore adlı Web uygulamasının üzerine yazılacak.</span><span class="sxs-lookup"><span data-stu-id="d5242-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="d5242-120">Silinmiş Web App ayarları geri yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="d5242-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="d5242-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5242-121">PARAMETERS</span></span>

### <span data-ttu-id="d5242-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="d5242-122">-AsJob</span></span>
<span data-ttu-id="d5242-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d5242-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5242-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5242-124">-DefaultProfile</span></span>
<span data-ttu-id="d5242-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5242-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5242-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d5242-126">-Force</span></span>
<span data-ttu-id="d5242-127">Geri yüklemeyi, onay istemeden yapın.</span><span class="sxs-lookup"><span data-stu-id="d5242-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d5242-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5242-128">-InputObject</span></span>
<span data-ttu-id="d5242-129">Silinen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d5242-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d5242-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5242-130">-Name</span></span>
<span data-ttu-id="d5242-131">Silinmiş Azure Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="d5242-131">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d5242-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5242-132">-ResourceGroupName</span></span>
<span data-ttu-id="d5242-133">Silinen Azure Web App 'in kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d5242-133">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d5242-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="d5242-134">-RestoreContentOnly</span></span>
<span data-ttu-id="d5242-135">Web uygulamasının dosyalarını geri yükleyin, ancak ayarları geri yüklemeyin.</span><span class="sxs-lookup"><span data-stu-id="d5242-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="d5242-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d5242-136">-Slot</span></span>
<span data-ttu-id="d5242-137">Silinen Azure Web App yuvası.</span><span class="sxs-lookup"><span data-stu-id="d5242-137">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="d5242-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="d5242-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="d5242-139">Yeni Azure Web App 'in App Service planı.</span><span class="sxs-lookup"><span data-stu-id="d5242-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="d5242-140">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="d5242-140">-TargetName</span></span>
<span data-ttu-id="d5242-141">Yeni Azure Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="d5242-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="d5242-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5242-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="d5242-143">Yeni Azure Web uygulamasını içeren kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d5242-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="d5242-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="d5242-144">-TargetSlot</span></span>
<span data-ttu-id="d5242-145">Yeni Azure Web App yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="d5242-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="d5242-146">-Usedeyıldız</span><span class="sxs-lookup"><span data-stu-id="d5242-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="d5242-147">Silinen bir uygulamayı çevrimdışı olan bir ölçeklendirme biriminden kurtarmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="d5242-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="d5242-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5242-148">-Confirm</span></span>
<span data-ttu-id="d5242-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5242-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5242-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5242-150">-WhatIf</span></span>
<span data-ttu-id="d5242-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5242-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5242-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5242-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5242-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5242-153">CommonParameters</span></span>
<span data-ttu-id="d5242-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5242-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5242-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5242-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5242-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5242-156">INPUTS</span></span>

### <span data-ttu-id="d5242-157">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d5242-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="d5242-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5242-158">OUTPUTS</span></span>

### <span data-ttu-id="d5242-159">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="d5242-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d5242-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5242-160">NOTES</span></span>

## <span data-ttu-id="d5242-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5242-161">RELATED LINKS</span></span>

[<span data-ttu-id="d5242-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d5242-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)