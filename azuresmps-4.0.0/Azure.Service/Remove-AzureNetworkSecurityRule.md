---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105869"
---
# <span data-ttu-id="45d58-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="45d58-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="45d58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d58-102">SYNOPSIS</span></span>
<span data-ttu-id="45d58-103">Ağ güvenlik grubundan bir ağ güvenliği kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45d58-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="45d58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45d58-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45d58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45d58-105">DESCRIPTION</span></span>
<span data-ttu-id="45d58-106">**Remove-AzureNetworkSecurityRule** cmdlet 'i, bir ağ güvenlik grubundan Azure ağ güvenliği kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45d58-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="45d58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45d58-107">EXAMPLES</span></span>

## <span data-ttu-id="45d58-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45d58-108">PARAMETERS</span></span>

### <span data-ttu-id="45d58-109">-Force</span><span class="sxs-lookup"><span data-stu-id="45d58-109">-Force</span></span>
<span data-ttu-id="45d58-110">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="45d58-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d58-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="45d58-111">-Name</span></span>
<span data-ttu-id="45d58-112">Bu cmdlet 'in kaldırdığı ağ güvenlik kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d58-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45d58-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="45d58-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="45d58-114">Bu cmdlet 'in değiştirdiği ağ güvenlik grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d58-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="45d58-115">**Inetworksecuritygroup** nesnesi edinmek için Get-AzureNetworkSecurityGroup cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="45d58-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45d58-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="45d58-116">-Profile</span></span>
<span data-ttu-id="45d58-117">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d58-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="45d58-118">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="45d58-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d58-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d58-119">CommonParameters</span></span>
<span data-ttu-id="45d58-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45d58-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d58-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d58-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d58-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45d58-122">INPUTS</span></span>

## <span data-ttu-id="45d58-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45d58-123">OUTPUTS</span></span>

## <span data-ttu-id="45d58-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45d58-124">NOTES</span></span>

## <span data-ttu-id="45d58-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45d58-125">RELATED LINKS</span></span>

[<span data-ttu-id="45d58-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="45d58-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


