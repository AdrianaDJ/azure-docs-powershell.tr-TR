---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938909"
---
# <span data-ttu-id="70956-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="70956-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="70956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70956-102">SYNOPSIS</span></span>
<span data-ttu-id="70956-103">Web uygulaması için sağlanan anlık görüntüleri alır.</span><span class="sxs-lookup"><span data-stu-id="70956-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70956-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70956-104">SYNTAX</span></span>

### <span data-ttu-id="70956-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="70956-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="70956-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="70956-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="70956-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="70956-107">DESCRIPTION</span></span>
<span data-ttu-id="70956-108">**Get-AzureRmWebAppSnapshot** cmdlet 'i, bir Web uygulamasının tüm anlık görüntülerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="70956-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="70956-109">Anlık görüntüler, Web uygulamasının dosyalarının ve ayarlarının otomatik yedeğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="70956-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="70956-110">**Restore-AzureRmWebAppSnapshot** cmdlet 'i ile anlık görüntü geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="70956-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="70956-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70956-111">EXAMPLES</span></span>

### <span data-ttu-id="70956-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70956-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="70956-113">"Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip "ConstosoApp" adlı bir Web uygulamasının anlık görüntülerini alma</span><span class="sxs-lookup"><span data-stu-id="70956-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="70956-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70956-114">PARAMETERS</span></span>

### <span data-ttu-id="70956-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70956-115">-DefaultProfile</span></span>
<span data-ttu-id="70956-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70956-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70956-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="70956-117">-Name</span></span>
<span data-ttu-id="70956-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="70956-118">The name of the web app.</span></span>

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

### <span data-ttu-id="70956-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70956-119">-ResourceGroupName</span></span>
<span data-ttu-id="70956-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="70956-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="70956-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="70956-121">-Slot</span></span>
<span data-ttu-id="70956-122">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="70956-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="70956-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="70956-123">-WebApp</span></span>
<span data-ttu-id="70956-124">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="70956-124">The web app object</span></span>

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

## <span data-ttu-id="70956-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70956-125">INPUTS</span></span>

### <span data-ttu-id="70956-126">System. String</span><span class="sxs-lookup"><span data-stu-id="70956-126">System.String</span></span>
<span data-ttu-id="70956-127">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="70956-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="70956-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70956-128">OUTPUTS</span></span>

### <span data-ttu-id="70956-129">Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="70956-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="70956-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70956-130">NOTES</span></span>

## <span data-ttu-id="70956-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70956-131">RELATED LINKS</span></span>

