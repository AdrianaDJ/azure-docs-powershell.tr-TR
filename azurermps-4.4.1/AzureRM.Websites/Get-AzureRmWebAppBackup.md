---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: b88386077cd1a1e7b934b2a05126f00fa76bec18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592155"
---
# <span data-ttu-id="1d567-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1d567-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="1d567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d567-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d567-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d567-103">SYNTAX</span></span>

### <span data-ttu-id="1d567-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1d567-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d567-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1d567-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d567-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d567-106">DESCRIPTION</span></span>
<span data-ttu-id="1d567-107">**Get-AzureRmWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="1d567-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="1d567-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d567-108">EXAMPLES</span></span>

### <span data-ttu-id="1d567-109">2</span><span class="sxs-lookup"><span data-stu-id="1d567-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="1d567-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adındaki Web uygulamasından KIMLIĞI "12345" olan yedeği alır.</span><span class="sxs-lookup"><span data-stu-id="1d567-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1d567-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d567-111">PARAMETERS</span></span>

### <span data-ttu-id="1d567-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="1d567-112">-BackupId</span></span>
<span data-ttu-id="1d567-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="1d567-113">Backup Id</span></span>

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

### <span data-ttu-id="1d567-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d567-114">-Name</span></span>
<span data-ttu-id="1d567-115">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="1d567-115">Webapp Name</span></span>

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

### <span data-ttu-id="1d567-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d567-116">-ResourceGroupName</span></span>
<span data-ttu-id="1d567-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1d567-117">Resource Group Name</span></span>

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

### <span data-ttu-id="1d567-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1d567-118">-Slot</span></span>
<span data-ttu-id="1d567-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="1d567-119">Slot Name</span></span>

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

### <span data-ttu-id="1d567-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1d567-120">-WebApp</span></span>
<span data-ttu-id="1d567-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="1d567-121">Piped WebApp</span></span>

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

### <span data-ttu-id="1d567-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d567-122">-DefaultProfile</span></span>
<span data-ttu-id="1d567-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d567-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d567-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d567-124">CommonParameters</span></span>
<span data-ttu-id="1d567-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d567-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d567-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d567-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d567-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d567-127">INPUTS</span></span>

### <span data-ttu-id="1d567-128">Bölge</span><span class="sxs-lookup"><span data-stu-id="1d567-128">Site</span></span>
<span data-ttu-id="1d567-129">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1d567-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1d567-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d567-130">OUTPUTS</span></span>

### <span data-ttu-id="1d567-131">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1d567-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="1d567-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d567-132">NOTES</span></span>

## <span data-ttu-id="1d567-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d567-133">RELATED LINKS</span></span>

