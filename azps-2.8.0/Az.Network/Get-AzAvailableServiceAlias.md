---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 7ea7bec01bacba43732f8e1eb544b109dfae11b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931782"
---
# <span data-ttu-id="21fa0-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="21fa0-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="21fa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="21fa0-103">Bölgede kullanılabilir hizmet diğer adlarını alma.</span><span class="sxs-lookup"><span data-stu-id="21fa0-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="21fa0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21fa0-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21fa0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="21fa0-106">**Get-AzAvailableServiceAlias** cmdlet 'i sağlanan konumdaki bir alt ağın tüm kullanılabilir hizmet diğer adlarını almanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="21fa0-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="21fa0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="21fa0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21fa0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAliases -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="21fa0-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21fa0-109">PARAMETERS</span></span>

### <span data-ttu-id="21fa0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fa0-110">-DefaultProfile</span></span>
<span data-ttu-id="21fa0-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21fa0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21fa0-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="21fa0-112">-Location</span></span>
<span data-ttu-id="21fa0-113">Konum.</span><span class="sxs-lookup"><span data-stu-id="21fa0-113">The location.</span></span>

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

### <span data-ttu-id="21fa0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fa0-114">CommonParameters</span></span>
<span data-ttu-id="21fa0-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21fa0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fa0-116">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="21fa0-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fa0-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21fa0-117">INPUTS</span></span>

### <span data-ttu-id="21fa0-118">System. String</span><span class="sxs-lookup"><span data-stu-id="21fa0-118">System.String</span></span>

## <span data-ttu-id="21fa0-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21fa0-119">OUTPUTS</span></span>

### <span data-ttu-id="21fa0-120">Microsoft. Azure. Commands. Network. model. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="21fa0-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="21fa0-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21fa0-121">NOTES</span></span>

## <span data-ttu-id="21fa0-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21fa0-122">RELATED LINKS</span></span>
