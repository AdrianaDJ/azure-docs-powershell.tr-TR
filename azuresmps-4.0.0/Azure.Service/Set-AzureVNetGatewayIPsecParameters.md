---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106036"
---
# <span data-ttu-id="762b8-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="762b8-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="762b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762b8-102">SYNOPSIS</span></span>
<span data-ttu-id="762b8-103">Sanal ağ geçidi ile yerel ağ sitesi arasındaki bağlantının IPSec parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="762b8-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="762b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="762b8-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="762b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="762b8-105">DESCRIPTION</span></span>
<span data-ttu-id="762b8-106">**Set-AzureVNetGatewayIPsecParameters** cmdlet 'i sanal ağ geçidi ile yerel bir ağ sitesi arasındaki bağlantının Internet Protokolü güvenliğini (IPSec) ve Internet Anahtar DEĞIŞIMI (IKE) parametrelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="762b8-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="762b8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="762b8-107">EXAMPLES</span></span>

## <span data-ttu-id="762b8-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="762b8-108">PARAMETERS</span></span>

### <span data-ttu-id="762b8-109">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="762b8-109">-EncryptionType</span></span>
<span data-ttu-id="762b8-110">Sanal ağ geçidi için şifreleme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="762b8-111">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="762b8-111">Valid values are:</span></span> 

- <span data-ttu-id="762b8-112">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="762b8-112">NoEncryption</span></span> 
- <span data-ttu-id="762b8-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="762b8-113">RequireEncryption</span></span>

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

### <span data-ttu-id="762b8-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="762b8-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="762b8-115">Bu cmdlet 'in IPSec ve ıKE parametrelerini yapılandırdığı yerel ağ sitesi bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

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

### <span data-ttu-id="762b8-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="762b8-116">-PfsGroup</span></span>
<span data-ttu-id="762b8-117">Kusursuz iletme gizliliği (PFS) grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="762b8-118">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="762b8-118">Valid values are:</span></span> 

- <span data-ttu-id="762b8-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="762b8-119">PFS1</span></span> 
- <span data-ttu-id="762b8-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="762b8-120">None</span></span>

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

### <span data-ttu-id="762b8-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="762b8-121">-Profile</span></span>
<span data-ttu-id="762b8-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="762b8-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="762b8-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="762b8-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="762b8-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="762b8-125">Güvenlik ilişkisinin (SA) boyutunu kilobayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762b8-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="762b8-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="762b8-127">Güvenlik ilişkisinin süresini saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-127">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762b8-128">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="762b8-128">-VNetName</span></span>
<span data-ttu-id="762b8-129">Bu cmdlet 'in bağlantı için IPSec parametrelerini ayarladığı sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="762b8-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="762b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762b8-130">CommonParameters</span></span>
<span data-ttu-id="762b8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="762b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762b8-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762b8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762b8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="762b8-133">INPUTS</span></span>

## <span data-ttu-id="762b8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="762b8-134">OUTPUTS</span></span>

## <span data-ttu-id="762b8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="762b8-135">NOTES</span></span>

## <span data-ttu-id="762b8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="762b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="762b8-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="762b8-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


