---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: 98ded2967c364955ab8b9dd38f316021649d0fc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589273"
---
# <span data-ttu-id="b92b6-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b92b6-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="b92b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b92b6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b92b6-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b92b6-103">SYNTAX</span></span>

### <span data-ttu-id="b92b6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b92b6-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b92b6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b92b6-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b92b6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="b92b6-106">DESCRIPTION</span></span>
<span data-ttu-id="b92b6-107">**Remove-AzureRmWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b92b6-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="b92b6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b92b6-108">EXAMPLES</span></span>

### <span data-ttu-id="b92b6-109">2</span><span class="sxs-lookup"><span data-stu-id="b92b6-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="b92b6-110">Bu komut, KIMLIĞI "12345" olan yedekleme ile yedekleme 'yi, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b92b6-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b92b6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b92b6-111">PARAMETERS</span></span>

### <span data-ttu-id="b92b6-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="b92b6-112">-BackupId</span></span>
<span data-ttu-id="b92b6-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="b92b6-113">Backup Id</span></span>

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

### <span data-ttu-id="b92b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92b6-114">-DefaultProfile</span></span>
<span data-ttu-id="b92b6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b92b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b92b6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b92b6-116">-Name</span></span>
<span data-ttu-id="b92b6-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="b92b6-117">WebApp Name</span></span>

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

### <span data-ttu-id="b92b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b92b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="b92b6-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b92b6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b92b6-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="b92b6-120">-Slot</span></span>
<span data-ttu-id="b92b6-121">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="b92b6-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b92b6-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b92b6-122">-WebApp</span></span>
<span data-ttu-id="b92b6-123">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="b92b6-123">WebApp Object</span></span>

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

### <span data-ttu-id="b92b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92b6-124">CommonParameters</span></span>
<span data-ttu-id="b92b6-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b92b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92b6-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b92b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92b6-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b92b6-127">INPUTS</span></span>

### <span data-ttu-id="b92b6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b92b6-128">System.String</span></span>

### <span data-ttu-id="b92b6-129">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="b92b6-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b92b6-130">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b92b6-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="b92b6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b92b6-131">OUTPUTS</span></span>

### <span data-ttu-id="b92b6-132">Microsoft. Azure. Management. Web. model. Yedeklemeöğesi</span><span class="sxs-lookup"><span data-stu-id="b92b6-132">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="b92b6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b92b6-133">NOTES</span></span>

## <span data-ttu-id="b92b6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b92b6-134">RELATED LINKS</span></span>
