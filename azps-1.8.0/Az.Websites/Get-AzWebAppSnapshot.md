---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: fab46f997492c366857c7d13bea38543cca4e91c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753821"
---
# <span data-ttu-id="4fd24-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4fd24-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="4fd24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd24-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd24-103">Web uygulaması için sağlanan anlık görüntüleri alır.</span><span class="sxs-lookup"><span data-stu-id="4fd24-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="4fd24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fd24-104">SYNTAX</span></span>

### <span data-ttu-id="4fd24-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4fd24-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fd24-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4fd24-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd24-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fd24-107">DESCRIPTION</span></span>
<span data-ttu-id="4fd24-108">**Get-AzWebAppSnapshot** cmdlet 'i, bir Web uygulamasının tüm anlık görüntülerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4fd24-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="4fd24-109">Anlık görüntüler, Web uygulamasının dosyalarının ve ayarlarının otomatik yedeğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="4fd24-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="4fd24-110">**Restore-AzWebAppSnapshot** cmdlet 'i ile anlık görüntü geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4fd24-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="4fd24-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fd24-111">EXAMPLES</span></span>

### <span data-ttu-id="4fd24-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4fd24-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="4fd24-113">"Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip "ConstosoApp" adlı bir Web uygulamasının anlık görüntülerini alma</span><span class="sxs-lookup"><span data-stu-id="4fd24-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="4fd24-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fd24-114">PARAMETERS</span></span>

### <span data-ttu-id="4fd24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd24-115">-DefaultProfile</span></span>
<span data-ttu-id="4fd24-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fd24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd24-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4fd24-117">-Name</span></span>
<span data-ttu-id="4fd24-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="4fd24-118">The name of the web app.</span></span>

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

### <span data-ttu-id="4fd24-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd24-119">-ResourceGroupName</span></span>
<span data-ttu-id="4fd24-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4fd24-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fd24-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4fd24-121">-Slot</span></span>
<span data-ttu-id="4fd24-122">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="4fd24-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="4fd24-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4fd24-123">-WebApp</span></span>
<span data-ttu-id="4fd24-124">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="4fd24-124">The web app object</span></span>

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

### <span data-ttu-id="4fd24-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd24-125">CommonParameters</span></span>
<span data-ttu-id="4fd24-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fd24-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd24-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd24-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd24-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fd24-128">INPUTS</span></span>

### <span data-ttu-id="4fd24-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4fd24-129">System.String</span></span>

### <span data-ttu-id="4fd24-130">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="4fd24-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4fd24-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fd24-131">OUTPUTS</span></span>

### <span data-ttu-id="4fd24-132">Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4fd24-132">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="4fd24-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fd24-133">NOTES</span></span>

## <span data-ttu-id="4fd24-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fd24-134">RELATED LINKS</span></span>
