---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589267"
---
# <span data-ttu-id="af33f-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="af33f-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="af33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af33f-102">SYNOPSIS</span></span>
<span data-ttu-id="af33f-103">Web uygulaması anlık görüntüsünü geri yükler.</span><span class="sxs-lookup"><span data-stu-id="af33f-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af33f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af33f-104">SYNTAX</span></span>

### <span data-ttu-id="af33f-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="af33f-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af33f-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="af33f-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af33f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af33f-107">DESCRIPTION</span></span>
<span data-ttu-id="af33f-108">Web uygulamasının anlık görüntüsünü Web uygulamasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="af33f-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="af33f-109">Anlık görüntünün geri yüklenmesi, bir Web uygulamasındaki dosyaların üzerine, anlık görüntüdeki dosyalarla yazar.</span><span class="sxs-lookup"><span data-stu-id="af33f-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="af33f-110">Ayarları da geri yüklemek için kurtarılan yapılandırma anahtarı parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="af33f-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="af33f-111">Bir Web uygulamasından anlık görüntü aynı abonelikteki başka bir Web uygulamasına geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="af33f-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="af33f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af33f-112">EXAMPLES</span></span>

### <span data-ttu-id="af33f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af33f-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="af33f-114">"ContosoApp" adlı bir Web uygulamasının en son anlık görüntüsünü "Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip alır.</span><span class="sxs-lookup"><span data-stu-id="af33f-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="af33f-115">Anlık görüntüyü Web uygulamasının "geri yükleme" yuvasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="af33f-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="af33f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af33f-116">PARAMETERS</span></span>

### <span data-ttu-id="af33f-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="af33f-117">-AsJob</span></span>
<span data-ttu-id="af33f-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="af33f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af33f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af33f-119">-DefaultProfile</span></span>
<span data-ttu-id="af33f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af33f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af33f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="af33f-121">-Force</span></span>
<span data-ttu-id="af33f-122">Özgün Web uygulamasının, uyarı görüntülemeden üzerine yazılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="af33f-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af33f-123">-InputObject</span></span>
<span data-ttu-id="af33f-124">Azure Web App anlık görüntüsü.</span><span class="sxs-lookup"><span data-stu-id="af33f-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="af33f-125">-Name</span></span>
<span data-ttu-id="af33f-126">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="af33f-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-127">-Recoveryapılandırma</span><span class="sxs-lookup"><span data-stu-id="af33f-127">-RecoverConfiguration</span></span>
<span data-ttu-id="af33f-128">Dosyalara ek olarak Web uygulamasının yapılandırmasını kurtarma.</span><span class="sxs-lookup"><span data-stu-id="af33f-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af33f-129">-ResourceGroupName</span></span>
<span data-ttu-id="af33f-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="af33f-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-131">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="af33f-131">-Slot</span></span>
<span data-ttu-id="af33f-132">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="af33f-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="af33f-133">-WebApp</span></span>
<span data-ttu-id="af33f-134">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="af33f-134">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af33f-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="af33f-135">-Confirm</span></span>
<span data-ttu-id="af33f-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af33f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af33f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af33f-137">-WhatIf</span></span>
<span data-ttu-id="af33f-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af33f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af33f-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af33f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af33f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af33f-140">CommonParameters</span></span>
<span data-ttu-id="af33f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af33f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af33f-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af33f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af33f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af33f-143">INPUTS</span></span>

### <span data-ttu-id="af33f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af33f-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="af33f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="af33f-145">System.String</span></span>

### <span data-ttu-id="af33f-146">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="af33f-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="af33f-147">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af33f-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="af33f-148">Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="af33f-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="af33f-149">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af33f-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="af33f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af33f-150">OUTPUTS</span></span>

### <span data-ttu-id="af33f-151">System. void</span><span class="sxs-lookup"><span data-stu-id="af33f-151">System.Void</span></span>

## <span data-ttu-id="af33f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af33f-152">NOTES</span></span>

## <span data-ttu-id="af33f-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af33f-153">RELATED LINKS</span></span>
