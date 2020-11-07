---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: b533d63e83d731dd5b95788609d32fa4cf7863f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936120"
---
# <span data-ttu-id="d63f2-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d63f2-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="d63f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d63f2-102">SYNOPSIS</span></span>

## <span data-ttu-id="d63f2-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d63f2-103">SYNTAX</span></span>

### <span data-ttu-id="d63f2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d63f2-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d63f2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d63f2-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d63f2-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d63f2-106">DESCRIPTION</span></span>
<span data-ttu-id="d63f2-107">**Get-AzWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="d63f2-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="d63f2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d63f2-108">EXAMPLES</span></span>

### <span data-ttu-id="d63f2-109">2</span><span class="sxs-lookup"><span data-stu-id="d63f2-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="d63f2-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adındaki Web uygulamasından KIMLIĞI "12345" olan yedeği alır.</span><span class="sxs-lookup"><span data-stu-id="d63f2-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d63f2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d63f2-111">PARAMETERS</span></span>

### <span data-ttu-id="d63f2-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="d63f2-112">-BackupId</span></span>
<span data-ttu-id="d63f2-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="d63f2-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d63f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63f2-114">-DefaultProfile</span></span>
<span data-ttu-id="d63f2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d63f2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d63f2-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d63f2-116">-Name</span></span>
<span data-ttu-id="d63f2-117">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="d63f2-117">Webapp Name</span></span>

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

### <span data-ttu-id="d63f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d63f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="d63f2-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d63f2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d63f2-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d63f2-120">-Slot</span></span>
<span data-ttu-id="d63f2-121">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="d63f2-121">Slot Name</span></span>

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

### <span data-ttu-id="d63f2-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d63f2-122">-WebApp</span></span>
<span data-ttu-id="d63f2-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="d63f2-123">Piped WebApp</span></span>

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

### <span data-ttu-id="d63f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63f2-124">CommonParameters</span></span>
<span data-ttu-id="d63f2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d63f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63f2-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d63f2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63f2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d63f2-127">INPUTS</span></span>

### <span data-ttu-id="d63f2-128">Bölge</span><span class="sxs-lookup"><span data-stu-id="d63f2-128">Site</span></span>
<span data-ttu-id="d63f2-129">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d63f2-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d63f2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d63f2-130">OUTPUTS</span></span>

### <span data-ttu-id="d63f2-131">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d63f2-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="d63f2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d63f2-132">NOTES</span></span>

## <span data-ttu-id="d63f2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d63f2-133">RELATED LINKS</span></span>

