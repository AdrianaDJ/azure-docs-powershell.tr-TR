---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589495"
---
# <span data-ttu-id="ebb74-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ebb74-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="ebb74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb74-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb74-103">Bir kaynak grubundaki veya abonelikteki sanal WAN veya tüm sanal WAN 'Lara sahip olur.</span><span class="sxs-lookup"><span data-stu-id="ebb74-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebb74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebb74-104">SYNTAX</span></span>

### <span data-ttu-id="ebb74-105">Listbysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ebb74-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb74-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb74-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebb74-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebb74-107">DESCRIPTION</span></span>
<span data-ttu-id="ebb74-108">Bir kaynak grubundaki veya abonelikteki sanal WAN veya tüm sanal WAN 'Lara sahip olur.</span><span class="sxs-lookup"><span data-stu-id="ebb74-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="ebb74-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebb74-109">EXAMPLES</span></span>

### <span data-ttu-id="ebb74-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ebb74-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="ebb74-111">Bu komut, testRG kaynak grubundaki myVirtualWAN adındaki sanal WAN 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="ebb74-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="ebb74-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebb74-112">PARAMETERS</span></span>

### <span data-ttu-id="ebb74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb74-113">-DefaultProfile</span></span>
<span data-ttu-id="ebb74-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ebb74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb74-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ebb74-115">-Name</span></span>
<span data-ttu-id="ebb74-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ebb74-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb74-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebb74-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ebb74-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb74-119">CommonParameters</span></span>
<span data-ttu-id="ebb74-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebb74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb74-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb74-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb74-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebb74-122">INPUTS</span></span>

### <span data-ttu-id="ebb74-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ebb74-123">None</span></span>

## <span data-ttu-id="ebb74-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebb74-124">OUTPUTS</span></span>

### <span data-ttu-id="ebb74-125">Microsoft. Azure. Commands. Network. model. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ebb74-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="ebb74-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebb74-126">NOTES</span></span>

## <span data-ttu-id="ebb74-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebb74-127">RELATED LINKS</span></span>
