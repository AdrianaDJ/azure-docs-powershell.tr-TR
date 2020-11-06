---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572554"
---
# <span data-ttu-id="d5748-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5748-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="d5748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5748-102">SYNOPSIS</span></span>
<span data-ttu-id="d5748-103">Web uygulaması için sağlanan anlık görüntüleri alır.</span><span class="sxs-lookup"><span data-stu-id="d5748-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5748-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5748-104">SYNTAX</span></span>

### <span data-ttu-id="d5748-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d5748-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5748-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d5748-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5748-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5748-107">DESCRIPTION</span></span>
<span data-ttu-id="d5748-108">**Get-AzureRmWebAppSnapshot** cmdlet 'i, bir Web uygulamasının tüm anlık görüntülerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d5748-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="d5748-109">Anlık görüntüler, Web uygulamasının dosyalarının ve ayarlarının otomatik yedeğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d5748-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="d5748-110">**Restore-AzureRmWebAppSnapshot** cmdlet 'i ile anlık görüntü geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="d5748-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="d5748-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5748-111">EXAMPLES</span></span>

### <span data-ttu-id="d5748-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5748-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="d5748-113">"Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip "ConstosoApp" adlı bir Web uygulamasının anlık görüntülerini alma</span><span class="sxs-lookup"><span data-stu-id="d5748-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="d5748-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5748-114">PARAMETERS</span></span>

### <span data-ttu-id="d5748-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5748-115">-DefaultProfile</span></span>
<span data-ttu-id="d5748-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5748-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5748-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5748-117">-Name</span></span>
<span data-ttu-id="d5748-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="d5748-118">The name of the web app.</span></span>

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

### <span data-ttu-id="d5748-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5748-119">-ResourceGroupName</span></span>
<span data-ttu-id="d5748-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d5748-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5748-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d5748-121">-Slot</span></span>
<span data-ttu-id="d5748-122">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="d5748-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="d5748-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d5748-123">-WebApp</span></span>
<span data-ttu-id="d5748-124">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="d5748-124">The web app object</span></span>

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

### <span data-ttu-id="d5748-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5748-125">CommonParameters</span></span>
<span data-ttu-id="d5748-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5748-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5748-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5748-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5748-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5748-128">INPUTS</span></span>

### <span data-ttu-id="d5748-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d5748-129">System.String</span></span>

### <span data-ttu-id="d5748-130">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="d5748-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="d5748-131">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5748-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="d5748-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5748-132">OUTPUTS</span></span>

### <span data-ttu-id="d5748-133">Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5748-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="d5748-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5748-134">NOTES</span></span>

## <span data-ttu-id="d5748-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5748-135">RELATED LINKS</span></span>
