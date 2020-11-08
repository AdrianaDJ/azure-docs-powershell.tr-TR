---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: 04184483d2bda7495014d3efd8ecf35b4d3b6864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096202"
---
# <span data-ttu-id="f3ff3-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f3ff3-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="f3ff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ff3-102">SYNOPSIS</span></span>

## <span data-ttu-id="f3ff3-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3ff3-103">SYNTAX</span></span>

### <span data-ttu-id="f3ff3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f3ff3-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3ff3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f3ff3-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ff3-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3ff3-106">DESCRIPTION</span></span>
<span data-ttu-id="f3ff3-107">**Remove-AzWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3ff3-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f3ff3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3ff3-108">EXAMPLES</span></span>

### <span data-ttu-id="f3ff3-109">2</span><span class="sxs-lookup"><span data-stu-id="f3ff3-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f3ff3-110">Bu komut, KIMLIĞI "12345" olan yedekleme ile yedekleme 'yi, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3ff3-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f3ff3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3ff3-111">PARAMETERS</span></span>

### <span data-ttu-id="f3ff3-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="f3ff3-112">-BackupId</span></span>
<span data-ttu-id="f3ff3-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="f3ff3-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ff3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ff3-114">-DefaultProfile</span></span>
<span data-ttu-id="f3ff3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3ff3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ff3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3ff3-116">-Name</span></span>
<span data-ttu-id="f3ff3-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="f3ff3-117">WebApp Name</span></span>

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

### <span data-ttu-id="f3ff3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ff3-118">-ResourceGroupName</span></span>
<span data-ttu-id="f3ff3-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f3ff3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f3ff3-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f3ff3-120">-Slot</span></span>
<span data-ttu-id="f3ff3-121">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="f3ff3-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f3ff3-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f3ff3-122">-WebApp</span></span>
<span data-ttu-id="f3ff3-123">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="f3ff3-123">WebApp Object</span></span>

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

### <span data-ttu-id="f3ff3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ff3-124">CommonParameters</span></span>
<span data-ttu-id="f3ff3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3ff3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ff3-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ff3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ff3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3ff3-127">INPUTS</span></span>

### <span data-ttu-id="f3ff3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f3ff3-128">System.String</span></span>

### <span data-ttu-id="f3ff3-129">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="f3ff3-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f3ff3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3ff3-130">OUTPUTS</span></span>

### <span data-ttu-id="f3ff3-131">Microsoft. Azure. Management. Web. model. Yedeklemeöğesi</span><span class="sxs-lookup"><span data-stu-id="f3ff3-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="f3ff3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3ff3-132">NOTES</span></span>

## <span data-ttu-id="f3ff3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3ff3-133">RELATED LINKS</span></span>