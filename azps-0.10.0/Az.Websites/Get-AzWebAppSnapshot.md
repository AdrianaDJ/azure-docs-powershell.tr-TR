---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936107"
---
# <span data-ttu-id="8d30f-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d30f-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="8d30f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d30f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d30f-103">Web uygulaması için sağlanan anlık görüntüleri alır.</span><span class="sxs-lookup"><span data-stu-id="8d30f-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="8d30f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d30f-104">SYNTAX</span></span>

### <span data-ttu-id="8d30f-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8d30f-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="8d30f-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8d30f-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="8d30f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d30f-107">DESCRIPTION</span></span>
<span data-ttu-id="8d30f-108">**Get-AzWebAppSnapshot** cmdlet 'i, bir Web uygulamasının tüm anlık görüntülerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8d30f-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="8d30f-109">Anlık görüntüler, Web uygulamasının dosyalarının ve ayarlarının otomatik yedeğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="8d30f-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="8d30f-110">**Restore-AzWebAppSnapshot** cmdlet 'i ile anlık görüntü geri yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8d30f-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="8d30f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d30f-111">EXAMPLES</span></span>

### <span data-ttu-id="8d30f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8d30f-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="8d30f-113">"Default-Web-WestUS" kaynak grubunda "hazırlama" adlı bir yuvaya sahip "ConstosoApp" adlı bir Web uygulamasının anlık görüntülerini alma</span><span class="sxs-lookup"><span data-stu-id="8d30f-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="8d30f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d30f-114">PARAMETERS</span></span>

### <span data-ttu-id="8d30f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d30f-115">-DefaultProfile</span></span>
<span data-ttu-id="8d30f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d30f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d30f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d30f-117">-Name</span></span>
<span data-ttu-id="8d30f-118">Web uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="8d30f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="8d30f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d30f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d30f-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8d30f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d30f-121">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="8d30f-121">-Slot</span></span>
<span data-ttu-id="8d30f-122">Web uygulaması yuvasının adı.</span><span class="sxs-lookup"><span data-stu-id="8d30f-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="8d30f-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8d30f-123">-WebApp</span></span>
<span data-ttu-id="8d30f-124">Web App nesnesi</span><span class="sxs-lookup"><span data-stu-id="8d30f-124">The web app object</span></span>

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

## <span data-ttu-id="8d30f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d30f-125">INPUTS</span></span>

### <span data-ttu-id="8d30f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8d30f-126">System.String</span></span>
<span data-ttu-id="8d30f-127">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="8d30f-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="8d30f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d30f-128">OUTPUTS</span></span>

### <span data-ttu-id="8d30f-129">Microsoft. Azure. Commands. WebApps. cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d30f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="8d30f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d30f-130">NOTES</span></span>

## <span data-ttu-id="8d30f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d30f-131">RELATED LINKS</span></span>

