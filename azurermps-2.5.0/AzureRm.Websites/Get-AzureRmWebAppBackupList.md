---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939030"
---
# <span data-ttu-id="6f7ac-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="6f7ac-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="6f7ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f7ac-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f7ac-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f7ac-103">SYNTAX</span></span>

### <span data-ttu-id="6f7ac-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6f7ac-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f7ac-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6f7ac-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f7ac-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f7ac-106">DESCRIPTION</span></span>
<span data-ttu-id="6f7ac-107">**Get-AzureRmWebAppBackupList** cmdlet 'ı bir Azure Web App yedeklemelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="6f7ac-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="6f7ac-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f7ac-108">EXAMPLES</span></span>

### <span data-ttu-id="6f7ac-109">2</span><span class="sxs-lookup"><span data-stu-id="6f7ac-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="6f7ac-110">Bu komut, WebApp kaynak grubuyla ilişkilendirilmiş WebApp WebAppStandard ile ilgili bir yedekleme listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="6f7ac-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="6f7ac-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f7ac-111">PARAMETERS</span></span>

### <span data-ttu-id="6f7ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7ac-112">-DefaultProfile</span></span>
<span data-ttu-id="6f7ac-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f7ac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f7ac-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f7ac-114">-Name</span></span>
<span data-ttu-id="6f7ac-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="6f7ac-115">WebApp Name</span></span>

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

### <span data-ttu-id="6f7ac-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7ac-116">-ResourceGroupName</span></span>
<span data-ttu-id="6f7ac-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6f7ac-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6f7ac-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="6f7ac-118">-Slot</span></span>
<span data-ttu-id="6f7ac-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="6f7ac-119">Slot name</span></span>

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

### <span data-ttu-id="6f7ac-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6f7ac-120">-WebApp</span></span>
<span data-ttu-id="6f7ac-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="6f7ac-121">Piped WebApp</span></span>

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

### <span data-ttu-id="6f7ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7ac-122">CommonParameters</span></span>
<span data-ttu-id="6f7ac-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f7ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7ac-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f7ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7ac-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f7ac-125">INPUTS</span></span>

### <span data-ttu-id="6f7ac-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="6f7ac-126">Site</span></span>
<span data-ttu-id="6f7ac-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6f7ac-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6f7ac-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f7ac-128">OUTPUTS</span></span>

### <span data-ttu-id="6f7ac-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="6f7ac-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="6f7ac-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f7ac-130">NOTES</span></span>

## <span data-ttu-id="6f7ac-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f7ac-131">RELATED LINKS</span></span>

