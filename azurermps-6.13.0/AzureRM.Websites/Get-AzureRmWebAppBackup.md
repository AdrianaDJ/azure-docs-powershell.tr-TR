---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 7b3e721adaa0389f1c2a75750d7bf36dfe4c2ac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761951"
---
# <span data-ttu-id="d21bc-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d21bc-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="d21bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d21bc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d21bc-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d21bc-103">SYNTAX</span></span>

### <span data-ttu-id="d21bc-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d21bc-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d21bc-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d21bc-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d21bc-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d21bc-106">DESCRIPTION</span></span>
<span data-ttu-id="d21bc-107">**Get-AzureRmWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="d21bc-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="d21bc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d21bc-108">EXAMPLES</span></span>

### <span data-ttu-id="d21bc-109">2</span><span class="sxs-lookup"><span data-stu-id="d21bc-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="d21bc-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adındaki Web uygulamasından KIMLIĞI "12345" olan yedeği alır.</span><span class="sxs-lookup"><span data-stu-id="d21bc-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d21bc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d21bc-111">PARAMETERS</span></span>

### <span data-ttu-id="d21bc-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="d21bc-112">-BackupId</span></span>
<span data-ttu-id="d21bc-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="d21bc-113">Backup Id</span></span>

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

### <span data-ttu-id="d21bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d21bc-114">-DefaultProfile</span></span>
<span data-ttu-id="d21bc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d21bc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d21bc-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d21bc-116">-Name</span></span>
<span data-ttu-id="d21bc-117">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="d21bc-117">Webapp Name</span></span>

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

### <span data-ttu-id="d21bc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d21bc-118">-ResourceGroupName</span></span>
<span data-ttu-id="d21bc-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d21bc-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d21bc-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d21bc-120">-Slot</span></span>
<span data-ttu-id="d21bc-121">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="d21bc-121">Slot Name</span></span>

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

### <span data-ttu-id="d21bc-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d21bc-122">-WebApp</span></span>
<span data-ttu-id="d21bc-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="d21bc-123">Piped WebApp</span></span>

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

### <span data-ttu-id="d21bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21bc-124">CommonParameters</span></span>
<span data-ttu-id="d21bc-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d21bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21bc-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d21bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21bc-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d21bc-127">INPUTS</span></span>

### <span data-ttu-id="d21bc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d21bc-128">System.String</span></span>

### <span data-ttu-id="d21bc-129">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="d21bc-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="d21bc-130">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d21bc-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="d21bc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d21bc-131">OUTPUTS</span></span>

### <span data-ttu-id="d21bc-132">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d21bc-132">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="d21bc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d21bc-133">NOTES</span></span>

## <span data-ttu-id="d21bc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d21bc-134">RELATED LINKS</span></span>
