---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594531"
---
# <span data-ttu-id="8a937-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8a937-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="8a937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a937-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a937-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a937-103">SYNTAX</span></span>

### <span data-ttu-id="8a937-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8a937-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a937-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8a937-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a937-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a937-106">DESCRIPTION</span></span>
<span data-ttu-id="8a937-107">**Remove-AzureRmWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a937-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="8a937-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a937-108">EXAMPLES</span></span>

### <span data-ttu-id="8a937-109">2</span><span class="sxs-lookup"><span data-stu-id="8a937-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="8a937-110">Bu komut, KIMLIĞI "12345" olan yedekleme ile yedekleme 'yi, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a937-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8a937-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a937-111">PARAMETERS</span></span>

### <span data-ttu-id="8a937-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="8a937-112">-BackupId</span></span>
<span data-ttu-id="8a937-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="8a937-113">Backup Id</span></span>

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

### <span data-ttu-id="8a937-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a937-114">-Name</span></span>
<span data-ttu-id="8a937-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8a937-115">WebApp Name</span></span>

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

### <span data-ttu-id="8a937-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a937-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a937-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8a937-117">Resource Group Name</span></span>

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

### <span data-ttu-id="8a937-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="8a937-118">-Slot</span></span>
<span data-ttu-id="8a937-119">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="8a937-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8a937-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8a937-120">-WebApp</span></span>
<span data-ttu-id="8a937-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8a937-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a937-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a937-122">-DefaultProfile</span></span>
<span data-ttu-id="8a937-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a937-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a937-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a937-124">CommonParameters</span></span>
<span data-ttu-id="8a937-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a937-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a937-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a937-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a937-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a937-127">INPUTS</span></span>

### <span data-ttu-id="8a937-128">Bölge</span><span class="sxs-lookup"><span data-stu-id="8a937-128">Site</span></span>
<span data-ttu-id="8a937-129">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8a937-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8a937-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a937-130">OUTPUTS</span></span>

### <span data-ttu-id="8a937-131">Microsoft. Azure. Management. Web. model. Yedeklemeöğesi</span><span class="sxs-lookup"><span data-stu-id="8a937-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="8a937-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a937-132">NOTES</span></span>

## <span data-ttu-id="8a937-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a937-133">RELATED LINKS</span></span>

