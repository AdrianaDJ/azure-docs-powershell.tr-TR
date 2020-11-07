---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763072"
---
# <span data-ttu-id="abf22-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf22-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="abf22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf22-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf22-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abf22-103">SYNTAX</span></span>

### <span data-ttu-id="abf22-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="abf22-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf22-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="abf22-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abf22-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="abf22-106">DESCRIPTION</span></span>
<span data-ttu-id="abf22-107">**Get-AzureRmWebAppBackupConfiguration** cmdlet 'ı bir Azure Web uygulamasının yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="abf22-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="abf22-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abf22-108">EXAMPLES</span></span>

### <span data-ttu-id="abf22-109">2</span><span class="sxs-lookup"><span data-stu-id="abf22-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="abf22-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="abf22-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="abf22-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abf22-111">PARAMETERS</span></span>

### <span data-ttu-id="abf22-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="abf22-112">-Name</span></span>
<span data-ttu-id="abf22-113">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="abf22-113">WebApp Name</span></span>

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

### <span data-ttu-id="abf22-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf22-114">-ResourceGroupName</span></span>
<span data-ttu-id="abf22-115">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="abf22-115">Resource Group Name</span></span>

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

### <span data-ttu-id="abf22-116">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="abf22-116">-Slot</span></span>
<span data-ttu-id="abf22-117">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="abf22-117">Slot Name</span></span>

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

### <span data-ttu-id="abf22-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="abf22-118">-WebApp</span></span>
<span data-ttu-id="abf22-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="abf22-119">WebApp Name</span></span>

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

### <span data-ttu-id="abf22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf22-120">-DefaultProfile</span></span>
<span data-ttu-id="abf22-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abf22-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf22-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf22-122">CommonParameters</span></span>
<span data-ttu-id="abf22-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abf22-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf22-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf22-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf22-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abf22-125">INPUTS</span></span>

### <span data-ttu-id="abf22-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="abf22-126">Site</span></span>
<span data-ttu-id="abf22-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="abf22-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="abf22-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abf22-128">OUTPUTS</span></span>

### <span data-ttu-id="abf22-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf22-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="abf22-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abf22-130">NOTES</span></span>

## <span data-ttu-id="abf22-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abf22-131">RELATED LINKS</span></span>

