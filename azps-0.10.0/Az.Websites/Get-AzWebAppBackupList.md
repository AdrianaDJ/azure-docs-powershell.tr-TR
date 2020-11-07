---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936118"
---
# <span data-ttu-id="d974e-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="d974e-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="d974e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d974e-102">SYNOPSIS</span></span>

## <span data-ttu-id="d974e-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d974e-103">SYNTAX</span></span>

### <span data-ttu-id="d974e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d974e-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d974e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d974e-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d974e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d974e-106">DESCRIPTION</span></span>
<span data-ttu-id="d974e-107">**Get-AzWebAppBackupList** cmdlet 'ı bir Azure Web App yedeklemelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d974e-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="d974e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d974e-108">EXAMPLES</span></span>

### <span data-ttu-id="d974e-109">2</span><span class="sxs-lookup"><span data-stu-id="d974e-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d974e-110">Bu komut, WebApp kaynak grubuyla ilişkilendirilmiş WebApp WebAppStandard ile ilgili bir yedekleme listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="d974e-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="d974e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d974e-111">PARAMETERS</span></span>

### <span data-ttu-id="d974e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d974e-112">-DefaultProfile</span></span>
<span data-ttu-id="d974e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d974e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d974e-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="d974e-114">-Name</span></span>
<span data-ttu-id="d974e-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d974e-115">WebApp Name</span></span>

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

### <span data-ttu-id="d974e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d974e-116">-ResourceGroupName</span></span>
<span data-ttu-id="d974e-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d974e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d974e-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d974e-118">-Slot</span></span>
<span data-ttu-id="d974e-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="d974e-119">Slot name</span></span>

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

### <span data-ttu-id="d974e-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d974e-120">-WebApp</span></span>
<span data-ttu-id="d974e-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="d974e-121">Piped WebApp</span></span>

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

### <span data-ttu-id="d974e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d974e-122">CommonParameters</span></span>
<span data-ttu-id="d974e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d974e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d974e-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d974e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d974e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d974e-125">INPUTS</span></span>

### <span data-ttu-id="d974e-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="d974e-126">Site</span></span>
<span data-ttu-id="d974e-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d974e-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d974e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d974e-128">OUTPUTS</span></span>

### <span data-ttu-id="d974e-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="d974e-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="d974e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d974e-130">NOTES</span></span>

## <span data-ttu-id="d974e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d974e-131">RELATED LINKS</span></span>

