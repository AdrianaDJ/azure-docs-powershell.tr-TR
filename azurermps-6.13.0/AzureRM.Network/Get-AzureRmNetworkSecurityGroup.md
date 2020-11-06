---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 32bcc3b83ad34a0f60b01048212d402745934317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595076"
---
# <span data-ttu-id="92de4-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92de4-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="92de4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92de4-102">SYNOPSIS</span></span>
<span data-ttu-id="92de4-103">Bir ağ güvenlik grubu alır.</span><span class="sxs-lookup"><span data-stu-id="92de4-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92de4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92de4-104">SYNTAX</span></span>

### <span data-ttu-id="92de4-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="92de4-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92de4-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="92de4-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92de4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="92de4-107">DESCRIPTION</span></span>
<span data-ttu-id="92de4-108">**Get-AzureRmNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="92de4-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="92de4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92de4-109">EXAMPLES</span></span>

### <span data-ttu-id="92de4-110">1: var olan bir ağ güvenlik grubunu alma</span><span class="sxs-lookup"><span data-stu-id="92de4-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="92de4-111">Bu komut, "RG1" kaynak grubundaki "nsg1" Azure ağ güvenlik grubunun içeriğini döndürüyor</span><span class="sxs-lookup"><span data-stu-id="92de4-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="92de4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92de4-112">PARAMETERS</span></span>

### <span data-ttu-id="92de4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92de4-113">-DefaultProfile</span></span>
<span data-ttu-id="92de4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92de4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92de4-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="92de4-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92de4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="92de4-116">-Name</span></span>
<span data-ttu-id="92de4-117">Bu cmdlet 'in aldığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92de4-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92de4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92de4-118">-ResourceGroupName</span></span>
<span data-ttu-id="92de4-119">Ağ güvenlik grubunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92de4-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92de4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92de4-120">CommonParameters</span></span>
<span data-ttu-id="92de4-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92de4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92de4-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92de4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92de4-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92de4-123">INPUTS</span></span>

### <span data-ttu-id="92de4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="92de4-124">System.String</span></span>

## <span data-ttu-id="92de4-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92de4-125">OUTPUTS</span></span>

### <span data-ttu-id="92de4-126">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92de4-126">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="92de4-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92de4-127">NOTES</span></span>

## <span data-ttu-id="92de4-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92de4-128">RELATED LINKS</span></span>

[<span data-ttu-id="92de4-129">Yeni-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92de4-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="92de4-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92de4-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="92de4-131">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="92de4-131">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


