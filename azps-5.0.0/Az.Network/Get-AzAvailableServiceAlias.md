---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278133"
---
# <span data-ttu-id="261f2-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="261f2-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="261f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="261f2-102">SYNOPSIS</span></span>
<span data-ttu-id="261f2-103">Bölgede kullanılabilir hizmet diğer adlarını alma.</span><span class="sxs-lookup"><span data-stu-id="261f2-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="261f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="261f2-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="261f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="261f2-105">DESCRIPTION</span></span>
<span data-ttu-id="261f2-106">**Get-AzAvailableServiceAlias** cmdlet 'i sağlanan konumdaki bir alt ağın tüm kullanılabilir hizmet diğer adlarını almanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="261f2-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="261f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="261f2-107">EXAMPLES</span></span>

### <span data-ttu-id="261f2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="261f2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="261f2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="261f2-109">PARAMETERS</span></span>

### <span data-ttu-id="261f2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261f2-110">-DefaultProfile</span></span>
<span data-ttu-id="261f2-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="261f2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="261f2-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="261f2-112">-Location</span></span>
<span data-ttu-id="261f2-113">Konum.</span><span class="sxs-lookup"><span data-stu-id="261f2-113">The location.</span></span>

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

### <span data-ttu-id="261f2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261f2-114">CommonParameters</span></span>
<span data-ttu-id="261f2-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="261f2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261f2-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="261f2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261f2-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="261f2-117">INPUTS</span></span>

### <span data-ttu-id="261f2-118">System. String</span><span class="sxs-lookup"><span data-stu-id="261f2-118">System.String</span></span>

## <span data-ttu-id="261f2-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="261f2-119">OUTPUTS</span></span>

### <span data-ttu-id="261f2-120">Microsoft. Azure. Commands. Network. model. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="261f2-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="261f2-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="261f2-121">NOTES</span></span>

## <span data-ttu-id="261f2-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="261f2-122">RELATED LINKS</span></span>
