---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1eadfabddc2b474890003c6afe3829e3622f2f29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753780"
---
# <span data-ttu-id="7609d-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7609d-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="7609d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7609d-102">SYNOPSIS</span></span>
<span data-ttu-id="7609d-103">Web uygulaması anlık görüntüsünü geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7609d-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="7609d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7609d-104">SYNTAX</span></span>

### <span data-ttu-id="7609d-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7609d-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7609d-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7609d-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7609d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7609d-107">DESCRIPTION</span></span>
<span data-ttu-id="7609d-108">Web uygulamasının anlık görüntüsünü Web uygulamasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7609d-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="7609d-109">Anlık görüntünün geri yüklenmesi, bir Web uygulamasındaki dosyaların üzerine, anlık görüntüdeki dosyalarla yazar.</span><span class="sxs-lookup"><span data-stu-id="7609d-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="7609d-110">Ayarları da geri yüklemek için kurtarılan yapılandırma anahtarı parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7609d-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="7609d-111">Bir Web uygulamasından anlık görüntü aynı abonelikteki başka bir Web uygulamasına geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="7609d-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="7609d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7609d-112">EXAMPLES</span></span>

### <span data-ttu-id="7609d-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7609d-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="7609d-114">"ContosoApp" adlı bir Web uygulamasının en son anlık görüntüsünü "Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip alır.</span><span class="sxs-lookup"><span data-stu-id="7609d-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="7609d-115">Anlık görüntüyü Web uygulamasının "geri yükleme" yuvasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7609d-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="7609d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7609d-116">PARAMETERS</span></span>

### <span data-ttu-id="7609d-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="7609d-117">-AsJob</span></span>
<span data-ttu-id="7609d-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7609d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7609d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7609d-119">-DefaultProfile</span></span>
<span data-ttu-id="7609d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7609d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7609d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7609d-121">-Force</span></span>
<span data-ttu-id="7609d-122">Özgün Web uygulamasının, uyarı görüntülemeden üzerine yazılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7609d-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="7609d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7609d-123">-InputObject</span></span>
<span data-ttu-id="7609d-124">Azure Web App anlık görüntüsü.</span><span class="sxs-lookup"><span data-stu-id="7609d-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="7609d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7609d-125">-Name</span></span>
<span data-ttu-id="7609d-126">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="7609d-126">The name of the web app.</span></span>

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

### <span data-ttu-id="7609d-127">-Recoveryapılandırma</span><span class="sxs-lookup"><span data-stu-id="7609d-127">-RecoverConfiguration</span></span>
<span data-ttu-id="7609d-128">Dosyalara ek olarak Web uygulamasının yapılandırmasını kurtarma.</span><span class="sxs-lookup"><span data-stu-id="7609d-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="7609d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7609d-129">-ResourceGroupName</span></span>
<span data-ttu-id="7609d-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7609d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7609d-131">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="7609d-131">-Slot</span></span>
<span data-ttu-id="7609d-132">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="7609d-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="7609d-133">-Usedeyıldız</span><span class="sxs-lookup"><span data-stu-id="7609d-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="7609d-134">Çevrimdışı olan bir ölçeklendirme biriminden anlık görüntüyü kurtarmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="7609d-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="7609d-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7609d-135">-WebApp</span></span>
<span data-ttu-id="7609d-136">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="7609d-136">The web app object</span></span>

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

### <span data-ttu-id="7609d-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="7609d-137">-Confirm</span></span>
<span data-ttu-id="7609d-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7609d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7609d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7609d-139">-WhatIf</span></span>
<span data-ttu-id="7609d-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7609d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7609d-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7609d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7609d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7609d-142">CommonParameters</span></span>
<span data-ttu-id="7609d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7609d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7609d-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7609d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7609d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7609d-145">INPUTS</span></span>

### <span data-ttu-id="7609d-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7609d-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7609d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7609d-147">System.String</span></span>

### <span data-ttu-id="7609d-148">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="7609d-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="7609d-149">Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7609d-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="7609d-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7609d-150">OUTPUTS</span></span>

### <span data-ttu-id="7609d-151">System. void</span><span class="sxs-lookup"><span data-stu-id="7609d-151">System.Void</span></span>

## <span data-ttu-id="7609d-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7609d-152">NOTES</span></span>

## <span data-ttu-id="7609d-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7609d-153">RELATED LINKS</span></span>
