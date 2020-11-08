---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106333"
---
# <span data-ttu-id="9e9e5-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="9e9e5-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="9e9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9e5-103">Ağ güvenlik grubunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="9e9e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e9e5-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e9e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e9e5-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9e5-106">**Get-AzureNetworkSecurityGroupConfig** cmdlet 'i, bir ağ güvenlik grubunun ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="9e9e5-107">Ağ güvenliği kurallarını görüntülemek için *ayrıntılı* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="9e9e5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e9e5-108">EXAMPLES</span></span>

## <span data-ttu-id="9e9e5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e9e5-109">PARAMETERS</span></span>

### <span data-ttu-id="9e9e5-110">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="9e9e5-110">-Detailed</span></span>
<span data-ttu-id="9e9e5-111">Bu cmdlet 'in ağ güvenlik kurallarını görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="9e9e5-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="9e9e5-112">-Profile</span></span>
<span data-ttu-id="9e9e5-113">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9e9e5-114">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e9e5-115">-VM</span><span class="sxs-lookup"><span data-stu-id="9e9e5-115">-VM</span></span>
<span data-ttu-id="9e9e5-116">Bu cmdlet 'in bir ağ güvenlik grubunun ayrıntılarını aldığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9e5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9e5-117">CommonParameters</span></span>
<span data-ttu-id="9e9e5-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e9e5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9e5-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9e5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9e5-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e9e5-120">INPUTS</span></span>

## <span data-ttu-id="9e9e5-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e9e5-121">OUTPUTS</span></span>

## <span data-ttu-id="9e9e5-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e9e5-122">NOTES</span></span>

## <span data-ttu-id="9e9e5-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e9e5-123">RELATED LINKS</span></span>

[<span data-ttu-id="9e9e5-124">Yeni-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9e9e5-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="9e9e5-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9e9e5-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


