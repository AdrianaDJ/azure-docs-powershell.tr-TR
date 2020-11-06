---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 895b020753d1f4191b87430b14e2b843a4524eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573137"
---
# <span data-ttu-id="50c75-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="50c75-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="50c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c75-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50c75-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50c75-103">SYNTAX</span></span>

### <span data-ttu-id="50c75-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="50c75-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50c75-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="50c75-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50c75-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="50c75-106">DESCRIPTION</span></span>
<span data-ttu-id="50c75-107">**Get-AzureRmWebAppBackupConfiguration** cmdlet 'ı bir Azure Web uygulamasının yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="50c75-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="50c75-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50c75-108">EXAMPLES</span></span>

### <span data-ttu-id="50c75-109">2</span><span class="sxs-lookup"><span data-stu-id="50c75-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="50c75-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="50c75-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="50c75-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50c75-111">PARAMETERS</span></span>

### <span data-ttu-id="50c75-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c75-112">-DefaultProfile</span></span>
<span data-ttu-id="50c75-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50c75-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c75-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="50c75-114">-Name</span></span>
<span data-ttu-id="50c75-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="50c75-115">WebApp Name</span></span>

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

### <span data-ttu-id="50c75-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c75-116">-ResourceGroupName</span></span>
<span data-ttu-id="50c75-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="50c75-117">Resource Group Name</span></span>

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

### <span data-ttu-id="50c75-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="50c75-118">-Slot</span></span>
<span data-ttu-id="50c75-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="50c75-119">Slot Name</span></span>

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

### <span data-ttu-id="50c75-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="50c75-120">-WebApp</span></span>
<span data-ttu-id="50c75-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="50c75-121">WebApp Name</span></span>

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

### <span data-ttu-id="50c75-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c75-122">CommonParameters</span></span>
<span data-ttu-id="50c75-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50c75-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c75-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c75-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c75-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50c75-125">INPUTS</span></span>

### <span data-ttu-id="50c75-126">Bölge</span><span class="sxs-lookup"><span data-stu-id="50c75-126">Site</span></span>
<span data-ttu-id="50c75-127">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="50c75-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="50c75-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50c75-128">OUTPUTS</span></span>

### <span data-ttu-id="50c75-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="50c75-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="50c75-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50c75-130">NOTES</span></span>

## <span data-ttu-id="50c75-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50c75-131">RELATED LINKS</span></span>

