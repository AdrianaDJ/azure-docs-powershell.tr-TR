---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106334"
---
# <span data-ttu-id="91929-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91929-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="91929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91929-102">SYNOPSIS</span></span>
<span data-ttu-id="91929-103">Ağ güvenlik grubunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="91929-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="91929-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91929-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91929-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91929-105">DESCRIPTION</span></span>
<span data-ttu-id="91929-106">**Get-AzureNetworkSecurityGroup** cmdlet 'ı bir Azure ağ güvenlik grubunun ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="91929-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="91929-107">Ağ güvenliği kurallarını görüntülemek için *ayrıntılı* parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="91929-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="91929-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91929-108">EXAMPLES</span></span>

## <span data-ttu-id="91929-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91929-109">PARAMETERS</span></span>

### <span data-ttu-id="91929-110">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="91929-110">-Detailed</span></span>
<span data-ttu-id="91929-111">Bu cmdlet 'in ağ güvenlik grubunun ağ güvenlik kurallarını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91929-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="91929-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="91929-112">-Name</span></span>
<span data-ttu-id="91929-113">Bu cmdlet 'in aldığı ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91929-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="91929-114">***Varsayılan ağ*** dışında bir kaynak grubunda, Azure portalı kullanılarak klasik bir ağ güvenlik grubu oluşturulduğunda, aşağıdaki PowerShell söz dizimini `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` kullanmalısınız:</span><span class="sxs-lookup"><span data-stu-id="91929-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91929-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="91929-115">-Profile</span></span>
<span data-ttu-id="91929-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91929-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91929-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="91929-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91929-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91929-118">CommonParameters</span></span>
<span data-ttu-id="91929-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91929-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91929-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91929-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91929-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91929-121">INPUTS</span></span>

## <span data-ttu-id="91929-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91929-122">OUTPUTS</span></span>

## <span data-ttu-id="91929-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91929-123">NOTES</span></span>

## <span data-ttu-id="91929-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91929-124">RELATED LINKS</span></span>

[<span data-ttu-id="91929-125">Yeni-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91929-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="91929-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91929-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

