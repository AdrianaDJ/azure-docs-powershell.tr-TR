---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266016"
---
# <span data-ttu-id="ba887-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ba887-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ba887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba887-102">SYNOPSIS</span></span>
<span data-ttu-id="ba887-103">Azure SecurityPartnerProvider alma</span><span class="sxs-lookup"><span data-stu-id="ba887-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ba887-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba887-104">SYNTAX</span></span>

### <span data-ttu-id="ba887-105">SecurityPartnerProviderNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba887-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba887-106">Securitypartnerproviderresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ba887-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba887-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba887-107">DESCRIPTION</span></span>
<span data-ttu-id="ba887-108">**Get-AzSecurityPartnerProvider** cmdlet 'ı bir Azure securitypartnerprovider alır</span><span class="sxs-lookup"><span data-stu-id="ba887-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ba887-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba887-109">EXAMPLES</span></span>

### <span data-ttu-id="ba887-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba887-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="ba887-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ba887-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="ba887-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba887-112">PARAMETERS</span></span>

### <span data-ttu-id="ba887-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba887-113">-DefaultProfile</span></span>
<span data-ttu-id="ba887-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba887-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba887-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba887-115">-Name</span></span>
<span data-ttu-id="ba887-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ba887-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba887-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba887-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba887-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ba887-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba887-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ba887-119">-ResourceId</span></span>
<span data-ttu-id="ba887-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ba887-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba887-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba887-121">CommonParameters</span></span>
<span data-ttu-id="ba887-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba887-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba887-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba887-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba887-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba887-124">INPUTS</span></span>

### <span data-ttu-id="ba887-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ba887-125">System.String</span></span>

## <span data-ttu-id="ba887-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba887-126">OUTPUTS</span></span>

### <span data-ttu-id="ba887-127">Microsoft. Azure. Commands. Network. model. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ba887-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ba887-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba887-128">NOTES</span></span>

## <span data-ttu-id="ba887-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba887-129">RELATED LINKS</span></span>
