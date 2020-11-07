---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: 194fcfddef0d85925bc08fb53fa7f5acf860e9ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937865"
---
# <span data-ttu-id="9f147-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="9f147-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="9f147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f147-102">SYNOPSIS</span></span>
<span data-ttu-id="9f147-103">Bir paylaşımın eşitleme ayarı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="9f147-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="9f147-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f147-104">SYNTAX</span></span>

### <span data-ttu-id="9f147-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f147-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f147-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9f147-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f147-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f147-107">DESCRIPTION</span></span>
<span data-ttu-id="9f147-108">**Get-Azdatasharesyntarihçe** cmdlet 'i, veri paylaşımı hesabı altındaki bir paylaşımda bulunan tüm eşitleme ayarları hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9f147-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="9f147-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f147-109">EXAMPLES</span></span>

### <span data-ttu-id="9f147-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f147-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="9f147-111">Bu komut, veri paylaşımı hesap WikiAds 'daki Share AdsShare dizininde bulunan tüm eşitleme ayarları hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9f147-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="9f147-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f147-112">PARAMETERS</span></span>

### <span data-ttu-id="9f147-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f147-113">-AccountName</span></span>
<span data-ttu-id="9f147-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="9f147-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f147-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f147-115">-DefaultProfile</span></span>
<span data-ttu-id="9f147-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f147-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f147-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f147-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f147-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9f147-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f147-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f147-119">-ResourceId</span></span>
<span data-ttu-id="9f147-120">Azure veri paylaşımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9f147-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f147-121">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="9f147-121">-ShareName</span></span>
<span data-ttu-id="9f147-122">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="9f147-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f147-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f147-123">CommonParameters</span></span>
<span data-ttu-id="9f147-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f147-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f147-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f147-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f147-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f147-126">INPUTS</span></span>

### <span data-ttu-id="9f147-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9f147-127">System.String</span></span>

## <span data-ttu-id="9f147-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f147-128">OUTPUTS</span></span>

### <span data-ttu-id="9f147-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşım</span><span class="sxs-lookup"><span data-stu-id="9f147-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="9f147-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f147-130">NOTES</span></span>

## <span data-ttu-id="9f147-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f147-131">RELATED LINKS</span></span>
