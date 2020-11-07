---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763071"
---
# <span data-ttu-id="f0a91-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="f0a91-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="f0a91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a91-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0a91-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0a91-103">SYNTAX</span></span>

### <span data-ttu-id="f0a91-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f0a91-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0a91-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f0a91-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a91-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0a91-106">DESCRIPTION</span></span>
<span data-ttu-id="f0a91-107">**Get-AzureRmWebAppBackupList** cmdlet 'ı bir Azure Web App yedeklemelerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f0a91-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="f0a91-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0a91-108">EXAMPLES</span></span>

### <span data-ttu-id="f0a91-109">2</span><span class="sxs-lookup"><span data-stu-id="f0a91-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="f0a91-110">Bu komut, WebApp kaynak grubuyla ilişkilendirilmiş WebApp WebAppStandard ile ilgili bir yedekleme listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0a91-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="f0a91-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0a91-111">PARAMETERS</span></span>

### <span data-ttu-id="f0a91-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0a91-112">-Name</span></span>
<span data-ttu-id="f0a91-113">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="f0a91-113">WebApp Name</span></span>

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

### <span data-ttu-id="f0a91-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a91-114">-ResourceGroupName</span></span>
<span data-ttu-id="f0a91-115">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f0a91-115">Resource Group Name</span></span>

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

### <span data-ttu-id="f0a91-116">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f0a91-116">-Slot</span></span>
<span data-ttu-id="f0a91-117">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="f0a91-117">Slot name</span></span>

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

### <span data-ttu-id="f0a91-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f0a91-118">-WebApp</span></span>
<span data-ttu-id="f0a91-119">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="f0a91-119">Piped WebApp</span></span>

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

### <span data-ttu-id="f0a91-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a91-120">-DefaultProfile</span></span>
<span data-ttu-id="f0a91-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0a91-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0a91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a91-122">CommonParameters</span></span>
<span data-ttu-id="f0a91-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0a91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a91-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a91-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a91-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0a91-125">INPUTS</span></span>

### <span data-ttu-id="f0a91-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="f0a91-126">Site</span></span>
<span data-ttu-id="f0a91-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f0a91-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f0a91-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0a91-128">OUTPUTS</span></span>

### <span data-ttu-id="f0a91-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="f0a91-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="f0a91-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0a91-130">NOTES</span></span>

## <span data-ttu-id="f0a91-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0a91-131">RELATED LINKS</span></span>

