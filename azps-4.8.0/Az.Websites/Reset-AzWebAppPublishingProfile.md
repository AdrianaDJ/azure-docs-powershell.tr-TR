---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109297"
---
# <span data-ttu-id="2516b-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2516b-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="2516b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2516b-102">SYNOPSIS</span></span>

## <span data-ttu-id="2516b-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2516b-103">SYNTAX</span></span>

### <span data-ttu-id="2516b-104">S1</span><span class="sxs-lookup"><span data-stu-id="2516b-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2516b-105">S2</span><span class="sxs-lookup"><span data-stu-id="2516b-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2516b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="2516b-106">DESCRIPTION</span></span>
<span data-ttu-id="2516b-107">**Reset-AzWebAppPublishingProfile** cmdlet 'i, belirtilen Web uygulamasının yayımlama profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="2516b-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="2516b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2516b-108">EXAMPLES</span></span>

### <span data-ttu-id="2516b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2516b-109">Example 1</span></span>

<span data-ttu-id="2516b-110">Aşağıdaki örnekte, MyResourceGroup kaynak grubuyla ilişkilendirilmiş Web App ıprule yayımlama profili sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="2516b-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="2516b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2516b-111">PARAMETERS</span></span>

### <span data-ttu-id="2516b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2516b-112">-DefaultProfile</span></span>
<span data-ttu-id="2516b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2516b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2516b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="2516b-114">-Name</span></span>
<span data-ttu-id="2516b-115">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="2516b-115">WebApp Name</span></span>

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

### <span data-ttu-id="2516b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2516b-116">-ResourceGroupName</span></span>
<span data-ttu-id="2516b-117">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2516b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="2516b-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2516b-118">-WebApp</span></span>
<span data-ttu-id="2516b-119">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="2516b-119">WebApp Object</span></span>

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

### <span data-ttu-id="2516b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2516b-120">CommonParameters</span></span>
<span data-ttu-id="2516b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2516b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2516b-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2516b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2516b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2516b-123">INPUTS</span></span>

### <span data-ttu-id="2516b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2516b-124">System.String</span></span>

### <span data-ttu-id="2516b-125">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="2516b-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2516b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2516b-126">OUTPUTS</span></span>

### <span data-ttu-id="2516b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2516b-127">System.String</span></span>

## <span data-ttu-id="2516b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2516b-128">NOTES</span></span>

## <span data-ttu-id="2516b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2516b-129">RELATED LINKS</span></span>
