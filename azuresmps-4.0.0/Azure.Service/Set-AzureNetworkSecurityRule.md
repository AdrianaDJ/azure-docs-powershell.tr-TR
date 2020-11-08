---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105800"
---
# <span data-ttu-id="ab3dd-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="ab3dd-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="ab3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3dd-103">Ağ güvenlik grubuna ağ güvenliği kuralı ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="ab3dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab3dd-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ab3dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3dd-106">**Set-AzureNetworkSecurityRule** cmdlet 'i, bir ağ güvenlik grubunda bir Azure ağ güvenliği kuralı ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="ab3dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab3dd-107">EXAMPLES</span></span>

## <span data-ttu-id="ab3dd-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab3dd-108">PARAMETERS</span></span>

### <span data-ttu-id="ab3dd-109">-Eylem</span><span class="sxs-lookup"><span data-stu-id="ab3dd-109">-Action</span></span>
<span data-ttu-id="ab3dd-110">Ağ güvenlik kuralı eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="ab3dd-111">Geçerli değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-111">Valid values are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab3dd-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="ab3dd-113">Ağ güvenlik kuralı için hedef IP aralığının sınıfsız etki alanları arası yönlendirme (CıDR) adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="ab3dd-114">Yıldız işareti (\*) herhangi bir IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-114">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="ab3dd-115">-DestinationPortRange</span></span>
<span data-ttu-id="ab3dd-116">Ağ güvenlik kuralı için bir hedef bağlantı noktası aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="ab3dd-117">Geçerli değerler 0 ile 65535 arasında tamsayılar içerir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="ab3dd-118">Tek bir değer belirtebilir ya da bir aralığı, küçük harf-HigherNumber biçiminde belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="ab3dd-119">Tire iki değeri birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-119">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab3dd-120">-Name</span></span>
<span data-ttu-id="ab3dd-121">Bu cmdlet 'in eklediği veya değiştirdiği ağ güvenlik kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ab3dd-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ab3dd-123">Bu cmdlet 'in değiştirdiği ağ güvenlik grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="ab3dd-124">**Inetworksecuritygroup** nesnesi edinmek için Get-AzureNetworkSecurityGroup cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

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

### <span data-ttu-id="ab3dd-125">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="ab3dd-125">-Priority</span></span>
<span data-ttu-id="ab3dd-126">Ağ güvenlik kuralının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="ab3dd-127">Geçerli değerler: 100 ile 4096 arasındaki tamsayılar.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab3dd-128">-Profile</span></span>
<span data-ttu-id="ab3dd-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ab3dd-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab3dd-131">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ab3dd-131">-Protocol</span></span>
<span data-ttu-id="ab3dd-132">Ağ güvenlik kuralı protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="ab3dd-133">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ab3dd-133">Valid values are:</span></span> 

- <span data-ttu-id="ab3dd-134">TC</span><span class="sxs-lookup"><span data-stu-id="ab3dd-134">TCP</span></span> 
- <span data-ttu-id="ab3dd-135">UDP</span><span class="sxs-lookup"><span data-stu-id="ab3dd-135">UDP</span></span> 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab3dd-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="ab3dd-137">Ağ güvenlik kuralı için kaynak IP aralığının CıDR adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="ab3dd-138">Yıldız işareti (\*) herhangi bir IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-138">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="ab3dd-139">-SourcePortRange</span></span>
<span data-ttu-id="ab3dd-140">Ağ güvenlik kuralı için bir kaynak bağlantı noktası aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="ab3dd-141">Geçerli değerler 0 ile 65535 arasında tamsayılar içerir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="ab3dd-142">Tek bir değer belirtebilir ya da bir aralığı, küçük harf-HigherNumber biçiminde belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="ab3dd-143">Tire iki değeri birbirinden ayırır.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-143">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-144">-Tür</span><span class="sxs-lookup"><span data-stu-id="ab3dd-144">-Type</span></span>
<span data-ttu-id="ab3dd-145">Ağ güvenlik kuralı için bağlantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="ab3dd-146">Geçerli değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-146">Valid values are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3dd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3dd-147">CommonParameters</span></span>
<span data-ttu-id="ab3dd-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab3dd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3dd-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3dd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3dd-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab3dd-150">INPUTS</span></span>

## <span data-ttu-id="ab3dd-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab3dd-151">OUTPUTS</span></span>

## <span data-ttu-id="ab3dd-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab3dd-152">NOTES</span></span>

## <span data-ttu-id="ab3dd-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab3dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="ab3dd-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="ab3dd-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


