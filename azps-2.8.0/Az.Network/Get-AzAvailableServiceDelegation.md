---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 547069954ada24531e1551b75c4065416eeae1fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932042"
---
# <span data-ttu-id="f2781-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="f2781-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="f2781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2781-102">SYNOPSIS</span></span>
<span data-ttu-id="f2781-103">Bölgede kullanılabilir hizmet temsilcilerini edinin.</span><span class="sxs-lookup"><span data-stu-id="f2781-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="f2781-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2781-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2781-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2781-105">DESCRIPTION</span></span>
<span data-ttu-id="f2781-106">**Get-AzAvailableServiceDelegation** cmdlet 'i, sağlanan konumdaki bir alt ağın tüm kullanılabilir hizmet temsilcilerini almanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f2781-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="f2781-107">Bu cmdlet, tek bir alt ağda birlikte bulunabilecek *temsilcileri açıklar.*</span><span class="sxs-lookup"><span data-stu-id="f2781-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="f2781-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2781-108">EXAMPLES</span></span>

### <span data-ttu-id="f2781-109">1: kullanılabilir tüm hizmet temsilcileri</span><span class="sxs-lookup"><span data-stu-id="f2781-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="f2781-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2781-110">PARAMETERS</span></span>

### <span data-ttu-id="f2781-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2781-111">-DefaultProfile</span></span>
<span data-ttu-id="f2781-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2781-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2781-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="f2781-113">-Location</span></span>
<span data-ttu-id="f2781-114">Konum.</span><span class="sxs-lookup"><span data-stu-id="f2781-114">The location.</span></span>

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

### <span data-ttu-id="f2781-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2781-115">CommonParameters</span></span>
<span data-ttu-id="f2781-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2781-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2781-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f2781-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2781-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2781-118">INPUTS</span></span>

### <span data-ttu-id="f2781-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f2781-119">System.String</span></span>

## <span data-ttu-id="f2781-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2781-120">OUTPUTS</span></span>

### <span data-ttu-id="f2781-121">Microsoft. Azure. Commands. Network. modeller. Psavailabletemsilci</span><span class="sxs-lookup"><span data-stu-id="f2781-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="f2781-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2781-122">NOTES</span></span>

## <span data-ttu-id="f2781-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2781-123">RELATED LINKS</span></span>

<span data-ttu-id="f2781-124">[Add-Aztemsilci](./Add-AzDelegation.md) 
 [Yeni-Aztemsilci](./New-AzDelegation.md) 
 [Remove-Aztemsilci](./Remove-AzDelegation.md) 
 [Get-Aztemsilci](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="f2781-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>