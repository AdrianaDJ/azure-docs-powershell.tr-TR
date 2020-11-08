---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 6a67fe30bfe6aaef21c094b126b9e1e3d92d468c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098395"
---
# <span data-ttu-id="8a8d6-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="8a8d6-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="8a8d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a8d6-102">SYNOPSIS</span></span>

## <span data-ttu-id="8a8d6-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a8d6-103">SYNTAX</span></span>

### <span data-ttu-id="8a8d6-104">S1</span><span class="sxs-lookup"><span data-stu-id="8a8d6-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a8d6-105">S2</span><span class="sxs-lookup"><span data-stu-id="8a8d6-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8d6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a8d6-106">DESCRIPTION</span></span>
<span data-ttu-id="8a8d6-107">**Reset-AzWebAppPublishingProfile** cmdlet 'i, belirtilen Web uygulamasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="8a8d6-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="8a8d6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a8d6-108">EXAMPLES</span></span>

### <span data-ttu-id="8a8d6-109">2</span><span class="sxs-lookup"><span data-stu-id="8a8d6-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="8a8d6-110">Bu komut, varsayılan-Web-WestUS kaynak grubuyla ilişkili Web App ContosoWebApp yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="8a8d6-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8a8d6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a8d6-111">PARAMETERS</span></span>

### <span data-ttu-id="8a8d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8d6-112">-DefaultProfile</span></span>
<span data-ttu-id="8a8d6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a8d6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a8d6-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a8d6-114">-Name</span></span>
<span data-ttu-id="8a8d6-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8a8d6-115">WebApp Name</span></span>

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

### <span data-ttu-id="8a8d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a8d6-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a8d6-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8a8d6-117">Resource Group Name</span></span>

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

### <span data-ttu-id="8a8d6-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8a8d6-118">-WebApp</span></span>
<span data-ttu-id="8a8d6-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8a8d6-119">WebApp Object</span></span>

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

### <span data-ttu-id="8a8d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8d6-120">CommonParameters</span></span>
<span data-ttu-id="8a8d6-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a8d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8d6-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8d6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8d6-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a8d6-123">INPUTS</span></span>

### <span data-ttu-id="8a8d6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8a8d6-124">System.String</span></span>

### <span data-ttu-id="8a8d6-125">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="8a8d6-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a8d6-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a8d6-126">OUTPUTS</span></span>

### <span data-ttu-id="8a8d6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8a8d6-127">System.String</span></span>

## <span data-ttu-id="8a8d6-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a8d6-128">NOTES</span></span>

## <span data-ttu-id="8a8d6-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a8d6-129">RELATED LINKS</span></span>
