---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105844"
---
# <span data-ttu-id="67889-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67889-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="67889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67889-102">SYNOPSIS</span></span>
<span data-ttu-id="67889-103">Uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="67889-103">Updates an application gateway.</span></span>

## <span data-ttu-id="67889-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67889-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="67889-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67889-105">DESCRIPTION</span></span>
<span data-ttu-id="67889-106">**Update-AzureApplicationGateway** cmdlet 'i var olan bir uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="67889-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="67889-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67889-107">EXAMPLES</span></span>

### <span data-ttu-id="67889-108">Örnek 1: adını kullanarak uygulama ağ geçidini değiştirme</span><span class="sxs-lookup"><span data-stu-id="67889-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="67889-109">İlk komut ApplicationGateway06 adlı uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="67889-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="67889-110">Sanal ağı veya alt ağları değiştirebilmeniz için bir uygulama ağ geçidi durdurulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="67889-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="67889-111">İkinci komut ApplicationGateway06 adlı uygulama ağ geçidinin sanal alt ağını ve alt ağlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="67889-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="67889-112">Örnek 2: uygulama ağ geçidinin ek özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="67889-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="67889-113">Bu komut, ApplicationGateway06 adlı uygulama ağ geçidinin örnek sayısını, ağ geçidi boyutunu ve açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="67889-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="67889-114">Bu komut, uygulama ağ geçidi için sanal ağı veya alt ağları değiştirmiyor.</span><span class="sxs-lookup"><span data-stu-id="67889-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="67889-115">Bu nedenle, bu komutu çalıştırmadan önce uygulama ağ geçidini durdurmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="67889-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="67889-116">Örnek 3: ardışık düzeni kullanarak uygulama ağ geçidini değiştirme</span><span class="sxs-lookup"><span data-stu-id="67889-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="67889-117">İlk komut **Get-AzureApplicationGateway** cmdlet 'Ini kullanarak ApplicationGateway06 adındaki uygulama ağ geçidini alır.</span><span class="sxs-lookup"><span data-stu-id="67889-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="67889-118">Komut, $ApplicationGateway değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="67889-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="67889-119">İkinci komut, ikinci değer olan **Gatewaysize** özelliğini atar.</span><span class="sxs-lookup"><span data-stu-id="67889-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="67889-120">Son komutu, güncelleştirilmiş $ApplicationGateway geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="67889-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="67889-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67889-121">PARAMETERS</span></span>

### <span data-ttu-id="67889-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="67889-122">-Description</span></span>
<span data-ttu-id="67889-123">Bu cmdlet 'in uygulama ağ geçidine atadığı açıklamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="67889-124">-Ağboyutu</span><span class="sxs-lookup"><span data-stu-id="67889-124">-GatewaySize</span></span>
<span data-ttu-id="67889-125">Bu cmdlet 'in uygulama ağ geçidine atadığı boyutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="67889-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="67889-126">Valid values are:</span></span>

- <span data-ttu-id="67889-127">Küçük</span><span class="sxs-lookup"><span data-stu-id="67889-127">Small</span></span>
- <span data-ttu-id="67889-128">Düzey</span><span class="sxs-lookup"><span data-stu-id="67889-128">Medium</span></span>
- <span data-ttu-id="67889-129">13</span><span class="sxs-lookup"><span data-stu-id="67889-129">Large</span></span>

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

### <span data-ttu-id="67889-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="67889-130">-InstanceCount</span></span>
<span data-ttu-id="67889-131">Bu cmdlet 'in uygulama ağ geçidine atadığı örnek sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="67889-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="67889-132">-Name</span></span>
<span data-ttu-id="67889-133">Bu cmdlet 'in güncelleştirdiği uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="67889-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="67889-134">-Profile</span></span>
<span data-ttu-id="67889-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67889-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="67889-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67889-137">-Alt ağlar</span><span class="sxs-lookup"><span data-stu-id="67889-137">-Subnets</span></span>
<span data-ttu-id="67889-138">Bu cmdlet 'in uygulama ağ geçidini dağıttığı alt ağ dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="67889-139">Uygulama ağ geçidi çalışırken alt ağları güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="67889-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="67889-140">Uygulama ağ geçidini durdurmak için Stop-AzureApplicationGateway cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="67889-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67889-141">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="67889-141">-VnetName</span></span>
<span data-ttu-id="67889-142">Bu cmdlet 'in uygulama ağ geçidini dağıtan sanal ağı belirtir.</span><span class="sxs-lookup"><span data-stu-id="67889-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="67889-143">Uygulama ağ geçidi çalışırken sanal bir ağı güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="67889-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="67889-144">Uygulama ağ geçidini durdurmak için **stop-AzureApplicationGateway** kullanın.</span><span class="sxs-lookup"><span data-stu-id="67889-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

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

### <span data-ttu-id="67889-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67889-145">CommonParameters</span></span>
<span data-ttu-id="67889-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67889-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67889-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67889-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67889-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67889-148">INPUTS</span></span>

### <span data-ttu-id="67889-149">System. String</span><span class="sxs-lookup"><span data-stu-id="67889-149">System.String</span></span>

## <span data-ttu-id="67889-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67889-150">OUTPUTS</span></span>

### <span data-ttu-id="67889-151">Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="67889-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="67889-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67889-152">NOTES</span></span>

## <span data-ttu-id="67889-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67889-153">RELATED LINKS</span></span>

[<span data-ttu-id="67889-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67889-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="67889-155">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67889-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="67889-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67889-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="67889-157">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67889-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="67889-158">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67889-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
