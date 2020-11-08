---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 8670581b376fe185ae4e477524f8f0a01c7cd3a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098394"
---
# <span data-ttu-id="107ac-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="107ac-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="107ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107ac-102">SYNOPSIS</span></span>

## <span data-ttu-id="107ac-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="107ac-103">SYNTAX</span></span>

### <span data-ttu-id="107ac-104">S1</span><span class="sxs-lookup"><span data-stu-id="107ac-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="107ac-105">S2</span><span class="sxs-lookup"><span data-stu-id="107ac-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="107ac-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="107ac-106">DESCRIPTION</span></span>
<span data-ttu-id="107ac-107">**Reset-AzWebAppSlotPublishingProfile** cmdlet 'i, belirtilen Web uygulaması yuvasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="107ac-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="107ac-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="107ac-108">EXAMPLES</span></span>

### <span data-ttu-id="107ac-109">2</span><span class="sxs-lookup"><span data-stu-id="107ac-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="107ac-110">Bu komut, Default-Web-WestUS kaynak grubuyla ilişkilendirilmiş Web App ContosoWebApp için slot001 adındaki yuva profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="107ac-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="107ac-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="107ac-111">PARAMETERS</span></span>

### <span data-ttu-id="107ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107ac-112">-DefaultProfile</span></span>
<span data-ttu-id="107ac-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="107ac-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="107ac-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="107ac-114">-Name</span></span>
<span data-ttu-id="107ac-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="107ac-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107ac-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107ac-116">-ResourceGroupName</span></span>
<span data-ttu-id="107ac-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="107ac-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107ac-118">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="107ac-118">-Slot</span></span>
<span data-ttu-id="107ac-119">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="107ac-119">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107ac-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="107ac-120">-WebApp</span></span>
<span data-ttu-id="107ac-121">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="107ac-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="107ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107ac-122">CommonParameters</span></span>
<span data-ttu-id="107ac-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="107ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107ac-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107ac-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107ac-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="107ac-125">INPUTS</span></span>

### <span data-ttu-id="107ac-126">System. String</span><span class="sxs-lookup"><span data-stu-id="107ac-126">System.String</span></span>

### <span data-ttu-id="107ac-127">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="107ac-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="107ac-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="107ac-128">OUTPUTS</span></span>

### <span data-ttu-id="107ac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="107ac-129">System.String</span></span>

## <span data-ttu-id="107ac-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="107ac-130">NOTES</span></span>

## <span data-ttu-id="107ac-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="107ac-131">RELATED LINKS</span></span>
