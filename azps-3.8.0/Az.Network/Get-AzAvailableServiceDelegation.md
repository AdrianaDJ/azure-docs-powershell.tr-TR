---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937433"
---
# <span data-ttu-id="edcae-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="edcae-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="edcae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edcae-102">SYNOPSIS</span></span>
<span data-ttu-id="edcae-103">Bölgede kullanılabilir hizmet temsilcilerini edinin.</span><span class="sxs-lookup"><span data-stu-id="edcae-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="edcae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edcae-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edcae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="edcae-105">DESCRIPTION</span></span>
<span data-ttu-id="edcae-106">**Get-AzAvailableServiceDelegation** cmdlet 'i, sağlanan konumdaki bir alt ağın tüm kullanılabilir hizmet temsilcilerini almanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="edcae-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="edcae-107">Bu cmdlet, tek bir alt ağda birlikte bulunabilecek *temsilcileri açıklar.*</span><span class="sxs-lookup"><span data-stu-id="edcae-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="edcae-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edcae-108">EXAMPLES</span></span>

### <span data-ttu-id="edcae-109">1: kullanılabilir tüm hizmet temsilcileri</span><span class="sxs-lookup"><span data-stu-id="edcae-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="edcae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edcae-110">PARAMETERS</span></span>

### <span data-ttu-id="edcae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcae-111">-DefaultProfile</span></span>
<span data-ttu-id="edcae-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edcae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edcae-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="edcae-113">-Location</span></span>
<span data-ttu-id="edcae-114">Konum.</span><span class="sxs-lookup"><span data-stu-id="edcae-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edcae-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcae-115">CommonParameters</span></span>
<span data-ttu-id="edcae-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edcae-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcae-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="edcae-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcae-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edcae-118">INPUTS</span></span>

### <span data-ttu-id="edcae-119">System. String</span><span class="sxs-lookup"><span data-stu-id="edcae-119">System.String</span></span>

## <span data-ttu-id="edcae-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edcae-120">OUTPUTS</span></span>

### <span data-ttu-id="edcae-121">Microsoft. Azure. Commands. Network. modeller. Psavailabletemsilci</span><span class="sxs-lookup"><span data-stu-id="edcae-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="edcae-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edcae-122">NOTES</span></span>

## <span data-ttu-id="edcae-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edcae-123">RELATED LINKS</span></span>

<span data-ttu-id="edcae-124">[Add-Aztemsilci](./Add-AzDelegation.md) 
 [Yeni-Aztemsilci](./New-AzDelegation.md) 
 [Remove-Aztemsilci](./Remove-AzDelegation.md) 
 [Get-Aztemsilci](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="edcae-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>