---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 65748ed269a7cb42914c98549c68be32812f71f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937604"
---
# <span data-ttu-id="f50f2-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f50f2-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="f50f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f50f2-102">SYNOPSIS</span></span>

## <span data-ttu-id="f50f2-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f50f2-103">SYNTAX</span></span>

### <span data-ttu-id="f50f2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f50f2-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f50f2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f50f2-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f50f2-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f50f2-106">DESCRIPTION</span></span>
<span data-ttu-id="f50f2-107">**Get-AzWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="f50f2-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f50f2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f50f2-108">EXAMPLES</span></span>

### <span data-ttu-id="f50f2-109">2</span><span class="sxs-lookup"><span data-stu-id="f50f2-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f50f2-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adındaki Web uygulamasından KIMLIĞI "12345" olan yedeği alır.</span><span class="sxs-lookup"><span data-stu-id="f50f2-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f50f2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f50f2-111">PARAMETERS</span></span>

### <span data-ttu-id="f50f2-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="f50f2-112">-BackupId</span></span>
<span data-ttu-id="f50f2-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="f50f2-113">Backup Id</span></span>

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

### <span data-ttu-id="f50f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50f2-114">-DefaultProfile</span></span>
<span data-ttu-id="f50f2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f50f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f50f2-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f50f2-116">-Name</span></span>
<span data-ttu-id="f50f2-117">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="f50f2-117">Webapp Name</span></span>

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

### <span data-ttu-id="f50f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="f50f2-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f50f2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f50f2-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f50f2-120">-Slot</span></span>
<span data-ttu-id="f50f2-121">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="f50f2-121">Slot Name</span></span>

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

### <span data-ttu-id="f50f2-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f50f2-122">-WebApp</span></span>
<span data-ttu-id="f50f2-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="f50f2-123">Piped WebApp</span></span>

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

### <span data-ttu-id="f50f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50f2-124">CommonParameters</span></span>
<span data-ttu-id="f50f2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f50f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50f2-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f50f2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50f2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f50f2-127">INPUTS</span></span>

### <span data-ttu-id="f50f2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f50f2-128">System.String</span></span>

### <span data-ttu-id="f50f2-129">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="f50f2-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f50f2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f50f2-130">OUTPUTS</span></span>

### <span data-ttu-id="f50f2-131">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f50f2-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="f50f2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f50f2-132">NOTES</span></span>

## <span data-ttu-id="f50f2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f50f2-133">RELATED LINKS</span></span>
