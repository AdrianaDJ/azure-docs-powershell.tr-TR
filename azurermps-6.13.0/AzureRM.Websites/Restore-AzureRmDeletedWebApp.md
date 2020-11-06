---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590772"
---
# <span data-ttu-id="b2d9a-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="b2d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d9a-103">Silinmiş bir Web uygulamasını yeni veya varolan bir Web uygulamasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2d9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2d9a-104">SYNTAX</span></span>

### <span data-ttu-id="b2d9a-105">Fromresourcename resourceName</span><span class="sxs-lookup"><span data-stu-id="b2d9a-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d9a-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="b2d9a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2d9a-107">DESCRIPTION</span></span>
<span data-ttu-id="b2d9a-108">**Restore-AzureRmDeletedWebApp** cmdlet 'i silinmiş bir Web uygulamasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="b2d9a-109">TargetResourceGroupName, hedefadı ve TargetSlot tarafından belirtilen Web uygulamasının üzerine, silinen Web uygulamasının içeriği ve ayarları yazılır.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="b2d9a-110">Hedef parametreler belirtilmemişse, otomatik olarak silinen Web uygulamasının kaynak grubu, adı ve yuvasına göre doldurulur.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="b2d9a-111">Hedef Web uygulaması yoksa, TargetAppServicePlanName tarafından belirtilen App Service planında otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="b2d9a-112">RestoreContentOnly Switch parametresi, uygulama ayarları olmadan yalnızca silinen uygulamanın dosyalarını geri yüklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="b2d9a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2d9a-113">EXAMPLES</span></span>

### <span data-ttu-id="b2d9a-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2d9a-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="b2d9a-115">Varsayılan-Web-WestUS kaynak grubuna ait olan ContosoApp adlı silinmiş bir uygulamayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="b2d9a-116">ContosoPlan adlı App Service planında aynı ada sahip ve kaynak grubuyla yeni bir uygulama oluşturulur ve silinen uygulamanın dosyaları ve ayarları bu dosyaya geri yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="b2d9a-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b2d9a-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="b2d9a-118">Varsayılan-Web-WestUS kaynak grubuna ait olan ContosoApp adlı silinen uygulamanın hazırlama yuvasını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="b2d9a-119">Varsayılan-Web-EastUS kaynak grubuna ait olan ContosoRestore adlı Web uygulamasının üzerine yazılacak.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="b2d9a-120">Silinmiş Web App ayarları geri yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="b2d9a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2d9a-121">PARAMETERS</span></span>

### <span data-ttu-id="b2d9a-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="b2d9a-122">-AsJob</span></span>
<span data-ttu-id="b2d9a-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b2d9a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2d9a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d9a-124">-DefaultProfile</span></span>
<span data-ttu-id="b2d9a-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2d9a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b2d9a-126">-Force</span></span>
<span data-ttu-id="b2d9a-127">Geri yüklemeyi, onay istemeden yapın.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b2d9a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2d9a-128">-InputObject</span></span>
<span data-ttu-id="b2d9a-129">Silinen Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2d9a-130">-Name</span></span>
<span data-ttu-id="b2d9a-131">Silinmiş Azure Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d9a-132">-ResourceGroupName</span></span>
<span data-ttu-id="b2d9a-133">Silinen Azure Web App 'in kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="b2d9a-134">-RestoreContentOnly</span></span>
<span data-ttu-id="b2d9a-135">Web uygulamasının dosyalarını geri yükleyin, ancak ayarları geri yüklemeyin.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="b2d9a-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="b2d9a-136">-Slot</span></span>
<span data-ttu-id="b2d9a-137">Silinen Azure Web App yuvası.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="b2d9a-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="b2d9a-139">Yeni Azure Web App 'in App Service planı.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-140">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="b2d9a-140">-TargetName</span></span>
<span data-ttu-id="b2d9a-141">Yeni Azure Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-141">The name of the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d9a-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="b2d9a-143">Yeni Azure Web uygulamasını içeren kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="b2d9a-144">-TargetSlot</span></span>
<span data-ttu-id="b2d9a-145">Yeni Azure Web App yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d9a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d9a-146">CommonParameters</span></span>
<span data-ttu-id="b2d9a-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2d9a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2d9a-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d9a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d9a-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2d9a-149">INPUTS</span></span>

### <span data-ttu-id="b2d9a-150">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="b2d9a-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2d9a-151">OUTPUTS</span></span>

### <span data-ttu-id="b2d9a-152">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="b2d9a-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b2d9a-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2d9a-153">NOTES</span></span>

## <span data-ttu-id="b2d9a-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2d9a-154">RELATED LINKS</span></span>

[<span data-ttu-id="b2d9a-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b2d9a-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
