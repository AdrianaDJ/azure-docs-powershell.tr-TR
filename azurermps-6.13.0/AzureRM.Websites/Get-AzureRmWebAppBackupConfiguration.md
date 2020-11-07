---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762086"
---
# <span data-ttu-id="a62ef-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a62ef-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="a62ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a62ef-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a62ef-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a62ef-103">SYNTAX</span></span>

### <span data-ttu-id="a62ef-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a62ef-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a62ef-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a62ef-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a62ef-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="a62ef-106">DESCRIPTION</span></span>
<span data-ttu-id="a62ef-107">**Get-AzureRmWebAppBackupConfiguration** cmdlet 'ı bir Azure Web uygulamasının yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="a62ef-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="a62ef-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a62ef-108">EXAMPLES</span></span>

### <span data-ttu-id="a62ef-109">2</span><span class="sxs-lookup"><span data-stu-id="a62ef-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="a62ef-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="a62ef-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a62ef-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a62ef-111">PARAMETERS</span></span>

### <span data-ttu-id="a62ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62ef-112">-DefaultProfile</span></span>
<span data-ttu-id="a62ef-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a62ef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a62ef-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a62ef-114">-Name</span></span>
<span data-ttu-id="a62ef-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="a62ef-115">WebApp Name</span></span>

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

### <span data-ttu-id="a62ef-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a62ef-116">-ResourceGroupName</span></span>
<span data-ttu-id="a62ef-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a62ef-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a62ef-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a62ef-118">-Slot</span></span>
<span data-ttu-id="a62ef-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="a62ef-119">Slot Name</span></span>

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

### <span data-ttu-id="a62ef-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a62ef-120">-WebApp</span></span>
<span data-ttu-id="a62ef-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="a62ef-121">WebApp Name</span></span>

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

### <span data-ttu-id="a62ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62ef-122">CommonParameters</span></span>
<span data-ttu-id="a62ef-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a62ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62ef-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62ef-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a62ef-125">INPUTS</span></span>

### <span data-ttu-id="a62ef-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a62ef-126">System.String</span></span>

### <span data-ttu-id="a62ef-127">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="a62ef-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a62ef-128">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a62ef-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a62ef-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a62ef-129">OUTPUTS</span></span>

### <span data-ttu-id="a62ef-130">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a62ef-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="a62ef-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a62ef-131">NOTES</span></span>

## <span data-ttu-id="a62ef-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a62ef-132">RELATED LINKS</span></span>
