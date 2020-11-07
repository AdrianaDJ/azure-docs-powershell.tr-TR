---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763444"
---
# <span data-ttu-id="48c7e-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="48c7e-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="48c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="48c7e-103">Bölgede kullanılabilir hizmet temsilcilerini edinin.</span><span class="sxs-lookup"><span data-stu-id="48c7e-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48c7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48c7e-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48c7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="48c7e-106">**Get-Azurermavailableservicetemsilci** cmdlet 'i, sağlanan konumda bir alt ağın tüm kullanılabilir hizmet temsilcilerini almanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="48c7e-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="48c7e-107">Bu cmdlet, tek bir alt ağda birlikte bulunabilecek *temsilcileri açıklar.*</span><span class="sxs-lookup"><span data-stu-id="48c7e-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="48c7e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48c7e-108">EXAMPLES</span></span>

### <span data-ttu-id="48c7e-109">1: kullanılabilir tüm hizmet temsilcileri</span><span class="sxs-lookup"><span data-stu-id="48c7e-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="48c7e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="48c7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c7e-111">-DefaultProfile</span></span>
<span data-ttu-id="48c7e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48c7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c7e-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="48c7e-113">-Location</span></span>
<span data-ttu-id="48c7e-114">Konum.</span><span class="sxs-lookup"><span data-stu-id="48c7e-114">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c7e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c7e-115">CommonParameters</span></span>
<span data-ttu-id="48c7e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48c7e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="48c7e-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c7e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c7e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48c7e-118">INPUTS</span></span>

### <span data-ttu-id="48c7e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="48c7e-119">System.String</span></span>

## <span data-ttu-id="48c7e-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48c7e-120">OUTPUTS</span></span>

### <span data-ttu-id="48c7e-121">Microsoft. Azure. Commands. Network. modeller. Psavailabletemsilci</span><span class="sxs-lookup"><span data-stu-id="48c7e-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="48c7e-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48c7e-122">NOTES</span></span>

## <span data-ttu-id="48c7e-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48c7e-123">RELATED LINKS</span></span>
<span data-ttu-id="48c7e-124">[Add-Azurermtemsilci](./Add-AzureRmDelegation.md) 
 [Yeni-Azurermtemsilci](./New-AzureRmDelegation.md) 
 [Remove-Azurermtemsilci](./Remove-AzureRmDelegation.md) 
 [Get-Azurermtemsilci](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="48c7e-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
