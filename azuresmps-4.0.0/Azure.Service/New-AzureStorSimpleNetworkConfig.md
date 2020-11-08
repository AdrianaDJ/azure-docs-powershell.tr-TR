---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105515"
---
# <span data-ttu-id="6a746-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="6a746-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="6a746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a746-102">SYNOPSIS</span></span>
<span data-ttu-id="6a746-103">Ağ yapılandırma nesnesini hazırlar.</span><span class="sxs-lookup"><span data-stu-id="6a746-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="6a746-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a746-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a746-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a746-105">DESCRIPTION</span></span>
<span data-ttu-id="6a746-106">**New-AzureStorSimpleNetworkConfig** cmdlet 'i, bir ağ yapılandırma nesnesini **set-AzureStorSimpleDevice** cmdlet 'ine geçirmek üzere hazırlar.</span><span class="sxs-lookup"><span data-stu-id="6a746-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="6a746-107">*Controller0IPAddress* parametresini ve *Controller1IPAddress* parametresini yalnızca data0 arabiriminde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6a746-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="6a746-108">Data0 yalnızca üç ayarı destekler: *Controller0IPAddress* , *Controller1IPAdress* ve *enableiscsı*.</span><span class="sxs-lookup"><span data-stu-id="6a746-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="6a746-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a746-109">EXAMPLES</span></span>

### <span data-ttu-id="6a746-110">Örnek 1: data0 arabirimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6a746-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="6a746-111">Bu komut data0 arabirimi için ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a746-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="6a746-112">Bu komut *Controller0IPv4Address* , *Controller1IPv4Address* ve *enableiscsı* parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="6a746-113">Bu cmdlet yalnızca bu üç parametre için data0 'i yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="6a746-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="6a746-114">Örnek 2: data0</span><span class="sxs-lookup"><span data-stu-id="6a746-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="6a746-115">Bu komut, Veri1 arabirimini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6a746-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="6a746-116">Örnek 3: aygıtın yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="6a746-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="6a746-117">İlk komut data0 arabirimi için bir ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a746-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="6a746-118">Bu komut *Controller0IPv4Address* , *Controller1IPv4Address* ve *enableiscsı* parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="6a746-119">Komut sonucu $NetworkConfigData 0 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="6a746-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="6a746-120">İkinci komut, çevrimiçi StorSimple aygıtı almak için **Get-AzureStorSimpleDevice** cmdlet 'Ini ve **WHERE-Object** Core cmdlet 'ini kullanır ve sonra da bunu $OnlineDevice değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6a746-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="6a746-121">Son komutu, **set-AzureStorSimpleDevice** cmdlet 'ini kullanarak BELIRTILEN cihaz kimliğine sahip aygıtın yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6a746-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="6a746-122">Komut, geçerli cmdlet 'in ilk komutta oluşturduğu yapılandırma nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a746-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="6a746-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a746-123">PARAMETERS</span></span>

### <span data-ttu-id="6a746-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="6a746-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="6a746-125">Denetleyicinin IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="6a746-126">Bu parametreyi yalnızca data0 arabirimi için belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a746-126">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="6a746-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="6a746-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="6a746-128">Denetleyici 1 için IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="6a746-129">Bu parametreyi yalnızca data0 arabirimi için belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a746-129">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="6a746-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="6a746-130">-EnableCloud</span></span>
<span data-ttu-id="6a746-131">Arabirimin bulut tarafından etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a746-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a746-132">-Enableiscsı</span><span class="sxs-lookup"><span data-stu-id="6a746-132">-EnableIscsi</span></span>
<span data-ttu-id="6a746-133">Arabirim için Internet SCSI (ISCSı) etkinleştirilip etkinleştirilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a746-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a746-134">-Interfacealias</span><span class="sxs-lookup"><span data-stu-id="6a746-134">-InterfaceAlias</span></span>
<span data-ttu-id="6a746-135">Bu cmdlet 'in ayarları sağladığı arabirimin arabirim diğer adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="6a746-136">Geçerli değerler data0 ile Data5 arasında.</span><span class="sxs-lookup"><span data-stu-id="6a746-136">Valid values are from Data0 to Data5.</span></span>

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

### <span data-ttu-id="6a746-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="6a746-137">-IPv4Address</span></span>
<span data-ttu-id="6a746-138">Arabirimin IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-138">Specifies the IPv4 address for the interface.</span></span>

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

### <span data-ttu-id="6a746-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="6a746-139">-IPv4Gateway</span></span>
<span data-ttu-id="6a746-140">Ağ geçidinin IPv4 adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-140">Specifies the IPv4 address of a gateway.</span></span>

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

### <span data-ttu-id="6a746-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="6a746-141">-IPv4Netmask</span></span>
<span data-ttu-id="6a746-142">Arabirim için IPv4 ağ maskesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-142">Specifies the IPv4 netmask for the interface.</span></span>

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

### <span data-ttu-id="6a746-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="6a746-143">-IPv6Gateway</span></span>
<span data-ttu-id="6a746-144">Arabirim için IPv6 ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-144">Specifies the IPv6 gateway for the interface.</span></span>

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

### <span data-ttu-id="6a746-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="6a746-145">-IPv6Prefix</span></span>
<span data-ttu-id="6a746-146">Arabirimin IPv6 önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-146">Specifies the IPv6 prefix for the interface.</span></span>

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

### <span data-ttu-id="6a746-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a746-147">-Profile</span></span>
<span data-ttu-id="6a746-148">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a746-148">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6a746-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a746-149">CommonParameters</span></span>
<span data-ttu-id="6a746-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a746-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a746-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a746-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a746-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a746-152">INPUTS</span></span>

### <span data-ttu-id="6a746-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6a746-153">None</span></span>

## <span data-ttu-id="6a746-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a746-154">OUTPUTS</span></span>

### <span data-ttu-id="6a746-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="6a746-155">NetworkConfig</span></span>
<span data-ttu-id="6a746-156">Bu cmdlet, aşağıdaki özellikleri içeren bir NetworkConfig nesnesi döndürür:</span><span class="sxs-lookup"><span data-stu-id="6a746-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="6a746-157">**Isiscsienabled** ( **Boole değeri** )</span><span class="sxs-lookup"><span data-stu-id="6a746-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="6a746-158">**Isalarbu** ( **Boole** )</span><span class="sxs-lookup"><span data-stu-id="6a746-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="6a746-159">**Controller0IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6a746-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6a746-160">**Controller1IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6a746-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6a746-161">**IPv6Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6a746-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6a746-162">**IPv4Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6a746-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6a746-163">**IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6a746-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6a746-164">**IPv6Prefix** ( **dize** )</span><span class="sxs-lookup"><span data-stu-id="6a746-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="6a746-165">**IPv4Netmask** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6a746-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6a746-166">**Interfacediğerad** ( **netınterfaceıd** )</span><span class="sxs-lookup"><span data-stu-id="6a746-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="6a746-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a746-167">NOTES</span></span>

## <span data-ttu-id="6a746-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a746-168">RELATED LINKS</span></span>

[<span data-ttu-id="6a746-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="6a746-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="6a746-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="6a746-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


