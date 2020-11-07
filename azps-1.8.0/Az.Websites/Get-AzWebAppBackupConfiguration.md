---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 3c48c913223d8122e7b26fe0e95db06f0e973ad1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753843"
---
# <span data-ttu-id="ec485-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec485-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ec485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec485-102">SYNOPSIS</span></span>

## <span data-ttu-id="ec485-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec485-103">SYNTAX</span></span>

### <span data-ttu-id="ec485-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ec485-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec485-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ec485-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec485-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec485-106">DESCRIPTION</span></span>
<span data-ttu-id="ec485-107">**Get-AzWebAppBackupConfiguration** cmdlet 'i, bir Azure Web uygulamasının yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec485-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="ec485-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec485-108">EXAMPLES</span></span>

### <span data-ttu-id="ec485-109">2</span><span class="sxs-lookup"><span data-stu-id="ec485-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="ec485-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec485-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ec485-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec485-111">PARAMETERS</span></span>

### <span data-ttu-id="ec485-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec485-112">-DefaultProfile</span></span>
<span data-ttu-id="ec485-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec485-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec485-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec485-114">-Name</span></span>
<span data-ttu-id="ec485-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ec485-115">WebApp Name</span></span>

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

### <span data-ttu-id="ec485-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec485-116">-ResourceGroupName</span></span>
<span data-ttu-id="ec485-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ec485-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ec485-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="ec485-118">-Slot</span></span>
<span data-ttu-id="ec485-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="ec485-119">Slot Name</span></span>

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

### <span data-ttu-id="ec485-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ec485-120">-WebApp</span></span>
<span data-ttu-id="ec485-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ec485-121">WebApp Name</span></span>

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

### <span data-ttu-id="ec485-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec485-122">CommonParameters</span></span>
<span data-ttu-id="ec485-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec485-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec485-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec485-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec485-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec485-125">INPUTS</span></span>

### <span data-ttu-id="ec485-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ec485-126">System.String</span></span>

### <span data-ttu-id="ec485-127">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="ec485-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec485-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec485-128">OUTPUTS</span></span>

### <span data-ttu-id="ec485-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec485-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ec485-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec485-130">NOTES</span></span>

## <span data-ttu-id="ec485-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec485-131">RELATED LINKS</span></span>
