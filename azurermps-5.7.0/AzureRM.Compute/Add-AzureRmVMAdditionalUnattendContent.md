---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589888"
---
# <span data-ttu-id="731a8-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="731a8-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="731a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731a8-102">SYNOPSIS</span></span>
<span data-ttu-id="731a8-103">Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="731a8-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="731a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="731a8-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="731a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="731a8-105">DESCRIPTION</span></span>
<span data-ttu-id="731a8-106">**Add-AzureRmVMAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="731a8-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="731a8-107">Bu cmdlet unattend.xml dosyaya eklediği ek temel 64 kodlanmış. xml biçimli bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="731a8-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="731a8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="731a8-108">EXAMPLES</span></span>

### <span data-ttu-id="731a8-109">Örnek 1: unattend.xml içerik ekleme</span><span class="sxs-lookup"><span data-stu-id="731a8-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="731a8-110">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="731a8-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="731a8-111">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="731a8-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="731a8-112">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="731a8-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="731a8-113">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="731a8-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="731a8-114">Üçüncü komut Get-Credential cmdlet 'ini kullanarak bir kimlik bilgisi nesnesi oluşturur ve sonucu $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="731a8-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="731a8-115">Komut sizden bir Kullanıcı adı ve parola ister.</span><span class="sxs-lookup"><span data-stu-id="731a8-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="731a8-116">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="731a8-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="731a8-117">Dördüncü komut, $VirtualMachine depolanan sanal makineyi yapılandırmak için **set-AzureRmVMOperatingSystem** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="731a8-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="731a8-118">Beşinci komut, $AucContent değişkenine içerik atar.</span><span class="sxs-lookup"><span data-stu-id="731a8-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="731a8-119">İçerik bir parola içerir.</span><span class="sxs-lookup"><span data-stu-id="731a8-119">The content includes a password.</span></span>

<span data-ttu-id="731a8-120">Son komut $AucContent depolanan içeriği unattend.xml dosyasına ekler.</span><span class="sxs-lookup"><span data-stu-id="731a8-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="731a8-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="731a8-121">PARAMETERS</span></span>

### <span data-ttu-id="731a8-122">-İçerik</span><span class="sxs-lookup"><span data-stu-id="731a8-122">-Content</span></span>
<span data-ttu-id="731a8-123">Base 64 kodlanmış XML formatlı içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="731a8-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="731a8-124">Bu cmdlet içeriği unattend.xml dosyasına ekler.</span><span class="sxs-lookup"><span data-stu-id="731a8-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="731a8-125">XML içeriği 4 KB 'den az olmalıdır ve bu cmdlet 'in eklediği ayarın veya özelliğin kök öğesini içermelidir.</span><span class="sxs-lookup"><span data-stu-id="731a8-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="731a8-126">-SettingName</span></span>
<span data-ttu-id="731a8-127">İçeriğin uygulandığı ayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="731a8-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="731a8-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="731a8-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="731a8-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="731a8-129">FirstLogonCommands</span></span>
- <span data-ttu-id="731a8-130">Açmayı</span><span class="sxs-lookup"><span data-stu-id="731a8-130">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-131">-VM</span><span class="sxs-lookup"><span data-stu-id="731a8-131">-VM</span></span>
<span data-ttu-id="731a8-132">Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="731a8-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="731a8-133">Sanal makine nesnesi edinmek için [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="731a8-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="731a8-134">[New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="731a8-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731a8-135">CommonParameters</span></span>
<span data-ttu-id="731a8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="731a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731a8-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731a8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731a8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="731a8-138">INPUTS</span></span>

### <span data-ttu-id="731a8-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="731a8-139">None</span></span>
<span data-ttu-id="731a8-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="731a8-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="731a8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="731a8-141">OUTPUTS</span></span>

## <span data-ttu-id="731a8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="731a8-142">NOTES</span></span>

## <span data-ttu-id="731a8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="731a8-143">RELATED LINKS</span></span>

[<span data-ttu-id="731a8-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="731a8-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="731a8-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="731a8-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="731a8-146">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="731a8-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
