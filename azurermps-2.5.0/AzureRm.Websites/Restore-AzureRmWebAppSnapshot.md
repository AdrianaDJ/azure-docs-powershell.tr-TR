---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939823"
---
# <span data-ttu-id="6d0b5-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6d0b5-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="6d0b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0b5-103">Web uygulaması anlık görüntüsünü geri yükler.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d0b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d0b5-104">SYNTAX</span></span>

### <span data-ttu-id="6d0b5-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6d0b5-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d0b5-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6d0b5-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d0b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d0b5-107">DESCRIPTION</span></span>
<span data-ttu-id="6d0b5-108">Web uygulamasının anlık görüntüsünü Web uygulamasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="6d0b5-109">Anlık görüntünün geri yüklenmesi, bir Web uygulamasındaki dosyaların üzerine, anlık görüntüdeki dosyalarla yazar.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="6d0b5-110">Ayarları da geri yüklemek için kurtarılan yapılandırma anahtarı parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="6d0b5-111">Bir Web uygulamasından anlık görüntü aynı abonelikteki başka bir Web uygulamasına geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="6d0b5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d0b5-112">EXAMPLES</span></span>

### <span data-ttu-id="6d0b5-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6d0b5-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="6d0b5-114">"ContosoApp" adlı bir Web uygulamasının en son anlık görüntüsünü "Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip alır.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="6d0b5-115">Anlık görüntüyü Web uygulamasının "geri yükleme" yuvasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="6d0b5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d0b5-116">PARAMETERS</span></span>

### <span data-ttu-id="6d0b5-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="6d0b5-117">-AsJob</span></span>
<span data-ttu-id="6d0b5-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6d0b5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d0b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0b5-119">-DefaultProfile</span></span>
<span data-ttu-id="6d0b5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d0b5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6d0b5-121">-Force</span></span>
<span data-ttu-id="6d0b5-122">Özgün Web uygulamasının, uyarı görüntülemeden üzerine yazılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d0b5-123">-InputObject</span></span>
<span data-ttu-id="6d0b5-124">Azure Web App anlık görüntüsü.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d0b5-125">-Name</span></span>
<span data-ttu-id="6d0b5-126">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-127">-Recoveryapılandırma</span><span class="sxs-lookup"><span data-stu-id="6d0b5-127">-RecoverConfiguration</span></span>
<span data-ttu-id="6d0b5-128">Dosyalara ek olarak Web uygulamasının yapılandırmasını kurtarma.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d0b5-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d0b5-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-131">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="6d0b5-131">-Slot</span></span>
<span data-ttu-id="6d0b5-132">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6d0b5-133">-WebApp</span></span>
<span data-ttu-id="6d0b5-134">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="6d0b5-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d0b5-135">-Confirm</span></span>
<span data-ttu-id="6d0b5-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d0b5-137">-WhatIf</span></span>
<span data-ttu-id="6d0b5-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d0b5-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d0b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0b5-140">CommonParameters</span></span>
<span data-ttu-id="6d0b5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d0b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0b5-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d0b5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0b5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d0b5-143">INPUTS</span></span>

### <span data-ttu-id="6d0b5-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d0b5-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="6d0b5-145">Microsoft. Azure. Management. Websiteleri. modeller. site System. String Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="6d0b5-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="6d0b5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d0b5-146">OUTPUTS</span></span>

### <span data-ttu-id="6d0b5-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="6d0b5-147">System.Object</span></span>

## <span data-ttu-id="6d0b5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d0b5-148">NOTES</span></span>

## <span data-ttu-id="6d0b5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d0b5-149">RELATED LINKS</span></span>

