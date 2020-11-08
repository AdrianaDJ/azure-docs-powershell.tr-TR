---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106226"
---
# <span data-ttu-id="48903-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48903-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="48903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48903-102">SYNOPSIS</span></span>
<span data-ttu-id="48903-103">Uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48903-103">Creates an application gateway.</span></span>

## <span data-ttu-id="48903-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48903-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="48903-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48903-105">DESCRIPTION</span></span>
<span data-ttu-id="48903-106">**New-AzureApplicationGateway** cmdlet 'i bir uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48903-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="48903-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48903-107">EXAMPLES</span></span>

### <span data-ttu-id="48903-108">Örnek 1: uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="48903-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="48903-109">Bu komut, ApplicationGateway06 adında bir uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48903-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="48903-110">Komut VirtualNetwork17 'de ve belirtilen alt ağlardaki ağ geçidini dağıtır.</span><span class="sxs-lookup"><span data-stu-id="48903-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="48903-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48903-111">PARAMETERS</span></span>

### <span data-ttu-id="48903-112">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="48903-112">-Description</span></span>
<span data-ttu-id="48903-113">Bu cmdlet 'in uygulama ağ geçidine atadığı açıklamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48903-114">-Ağboyutu</span><span class="sxs-lookup"><span data-stu-id="48903-114">-GatewaySize</span></span>
<span data-ttu-id="48903-115">Bu cmdlet 'in uygulama ağ geçidine atadığı boyutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="48903-116">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="48903-116">Valid values are:</span></span>

- <span data-ttu-id="48903-117">Küçük</span><span class="sxs-lookup"><span data-stu-id="48903-117">Small</span></span>
- <span data-ttu-id="48903-118">Düzey</span><span class="sxs-lookup"><span data-stu-id="48903-118">Medium</span></span>
- <span data-ttu-id="48903-119">13</span><span class="sxs-lookup"><span data-stu-id="48903-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48903-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="48903-120">-InstanceCount</span></span>
<span data-ttu-id="48903-121">Bu cmdlet 'in uygulama ağ geçidine atadığı örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48903-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="48903-122">-Name</span></span>
<span data-ttu-id="48903-123">Yeni uygulama ağ geçidi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-123">Specifies a name for the new application gateway.</span></span>

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

### <span data-ttu-id="48903-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="48903-124">-Profile</span></span>
<span data-ttu-id="48903-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48903-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="48903-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48903-127">-Alt ağlar</span><span class="sxs-lookup"><span data-stu-id="48903-127">-Subnets</span></span>
<span data-ttu-id="48903-128">Bu cmdlet 'in uygulama ağ geçidini dağıttığı alt ağ dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48903-129">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="48903-129">-VnetName</span></span>
<span data-ttu-id="48903-130">Bu cmdlet 'in uygulama ağ geçidini dağıtan sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="48903-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

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

### <span data-ttu-id="48903-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48903-131">CommonParameters</span></span>
<span data-ttu-id="48903-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48903-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48903-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48903-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48903-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48903-134">INPUTS</span></span>

### <span data-ttu-id="48903-135">System. String</span><span class="sxs-lookup"><span data-stu-id="48903-135">System.String</span></span>

## <span data-ttu-id="48903-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48903-136">OUTPUTS</span></span>

### <span data-ttu-id="48903-137">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="48903-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="48903-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48903-138">NOTES</span></span>

## <span data-ttu-id="48903-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48903-139">RELATED LINKS</span></span>

[<span data-ttu-id="48903-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48903-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="48903-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48903-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="48903-142">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48903-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="48903-143">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48903-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="48903-144">Güncelleştirme-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48903-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
