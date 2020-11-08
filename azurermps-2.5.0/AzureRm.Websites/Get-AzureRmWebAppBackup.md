---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: c6d5809211910987e06cff024d7510a70ad71a4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938751"
---
# <span data-ttu-id="1f66e-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1f66e-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="1f66e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f66e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f66e-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f66e-103">SYNTAX</span></span>

### <span data-ttu-id="1f66e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1f66e-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f66e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1f66e-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f66e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f66e-106">DESCRIPTION</span></span>
<span data-ttu-id="1f66e-107">**Get-AzureRmWebAppBackup** cmdlet 'ı bir Azure Web uygulamasının belirtilen yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="1f66e-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="1f66e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f66e-108">EXAMPLES</span></span>

### <span data-ttu-id="1f66e-109">2</span><span class="sxs-lookup"><span data-stu-id="1f66e-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="1f66e-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adındaki Web uygulamasından KIMLIĞI "12345" olan yedeği alır.</span><span class="sxs-lookup"><span data-stu-id="1f66e-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1f66e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f66e-111">PARAMETERS</span></span>

### <span data-ttu-id="1f66e-112">-BackupID</span><span class="sxs-lookup"><span data-stu-id="1f66e-112">-BackupId</span></span>
<span data-ttu-id="1f66e-113">Yedekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="1f66e-113">Backup Id</span></span>

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

### <span data-ttu-id="1f66e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f66e-114">-DefaultProfile</span></span>
<span data-ttu-id="1f66e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f66e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f66e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f66e-116">-Name</span></span>
<span data-ttu-id="1f66e-117">WEBAPP adı</span><span class="sxs-lookup"><span data-stu-id="1f66e-117">Webapp Name</span></span>

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

### <span data-ttu-id="1f66e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f66e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1f66e-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1f66e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1f66e-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1f66e-120">-Slot</span></span>
<span data-ttu-id="1f66e-121">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="1f66e-121">Slot Name</span></span>

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

### <span data-ttu-id="1f66e-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1f66e-122">-WebApp</span></span>
<span data-ttu-id="1f66e-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="1f66e-123">Piped WebApp</span></span>

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

### <span data-ttu-id="1f66e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f66e-124">CommonParameters</span></span>
<span data-ttu-id="1f66e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f66e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f66e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f66e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f66e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f66e-127">INPUTS</span></span>

### <span data-ttu-id="1f66e-128">Bölge</span><span class="sxs-lookup"><span data-stu-id="1f66e-128">Site</span></span>
<span data-ttu-id="1f66e-129">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1f66e-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1f66e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f66e-130">OUTPUTS</span></span>

### <span data-ttu-id="1f66e-131">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1f66e-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="1f66e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f66e-132">NOTES</span></span>

## <span data-ttu-id="1f66e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f66e-133">RELATED LINKS</span></span>
