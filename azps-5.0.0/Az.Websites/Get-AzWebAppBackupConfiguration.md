---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322561"
---
# <span data-ttu-id="803ed-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="803ed-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="803ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="803ed-102">SYNOPSIS</span></span>

## <span data-ttu-id="803ed-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="803ed-103">SYNTAX</span></span>

### <span data-ttu-id="803ed-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="803ed-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="803ed-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="803ed-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="803ed-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="803ed-106">DESCRIPTION</span></span>
<span data-ttu-id="803ed-107">**Get-AzWebAppBackupConfiguration** cmdlet 'i, bir Azure Web uygulamasının yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="803ed-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="803ed-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="803ed-108">EXAMPLES</span></span>

### <span data-ttu-id="803ed-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="803ed-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="803ed-110">Bu komut, varsayılan-Web-WestUS kaynak grubuna ait olan WebAppStandard adlı Web uygulamasından yedekleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="803ed-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="803ed-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="803ed-111">PARAMETERS</span></span>

### <span data-ttu-id="803ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803ed-112">-DefaultProfile</span></span>
<span data-ttu-id="803ed-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="803ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="803ed-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="803ed-114">-Name</span></span>
<span data-ttu-id="803ed-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="803ed-115">WebApp Name</span></span>

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

### <span data-ttu-id="803ed-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="803ed-116">-ResourceGroupName</span></span>
<span data-ttu-id="803ed-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="803ed-117">Resource Group Name</span></span>

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

### <span data-ttu-id="803ed-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="803ed-118">-Slot</span></span>
<span data-ttu-id="803ed-119">Yuva adı</span><span class="sxs-lookup"><span data-stu-id="803ed-119">Slot Name</span></span>

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

### <span data-ttu-id="803ed-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="803ed-120">-WebApp</span></span>
<span data-ttu-id="803ed-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="803ed-121">WebApp Name</span></span>

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

### <span data-ttu-id="803ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803ed-122">CommonParameters</span></span>
<span data-ttu-id="803ed-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="803ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803ed-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="803ed-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803ed-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="803ed-125">INPUTS</span></span>

### <span data-ttu-id="803ed-126">System. String</span><span class="sxs-lookup"><span data-stu-id="803ed-126">System.String</span></span>

### <span data-ttu-id="803ed-127">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="803ed-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="803ed-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="803ed-128">OUTPUTS</span></span>

### <span data-ttu-id="803ed-129">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="803ed-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="803ed-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="803ed-130">NOTES</span></span>

## <span data-ttu-id="803ed-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="803ed-131">RELATED LINKS</span></span>
