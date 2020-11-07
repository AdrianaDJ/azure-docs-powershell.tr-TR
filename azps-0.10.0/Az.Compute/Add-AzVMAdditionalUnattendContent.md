---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935207"
---
# <span data-ttu-id="57734-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="57734-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="57734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57734-102">SYNOPSIS</span></span>
<span data-ttu-id="57734-103">Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="57734-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="57734-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57734-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57734-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57734-105">DESCRIPTION</span></span>
<span data-ttu-id="57734-106">**Add-AzVMAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.</span><span class="sxs-lookup"><span data-stu-id="57734-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="57734-107">Bu cmdlet unattend.xml dosyaya eklediği ek temel 64 kodlanmış. xml biçimli bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="57734-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="57734-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57734-108">EXAMPLES</span></span>

### <span data-ttu-id="57734-109">Örnek 1: unattend.xml içerik ekleme</span><span class="sxs-lookup"><span data-stu-id="57734-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="57734-110">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57734-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="57734-111">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57734-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="57734-112">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="57734-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="57734-113">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="57734-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="57734-114">Üçüncü komut Get-Credential cmdlet 'ini kullanarak bir kimlik bilgisi nesnesi oluşturur ve sonucu $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57734-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="57734-115">Komut sizden bir Kullanıcı adı ve parola ister.</span><span class="sxs-lookup"><span data-stu-id="57734-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="57734-116">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="57734-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="57734-117">Dördüncü komut, $VirtualMachine depolanan sanal makineyi yapılandırmak için **set-AzVMOperatingSystem** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="57734-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="57734-118">Beşinci komut, $AucContent değişkenine içerik atar.</span><span class="sxs-lookup"><span data-stu-id="57734-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="57734-119">İçerik bir parola içerir.</span><span class="sxs-lookup"><span data-stu-id="57734-119">The content includes a password.</span></span>

<span data-ttu-id="57734-120">Son komut $AucContent depolanan içeriği unattend.xml dosyasına ekler.</span><span class="sxs-lookup"><span data-stu-id="57734-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="57734-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57734-121">PARAMETERS</span></span>

### <span data-ttu-id="57734-122">-İçerik</span><span class="sxs-lookup"><span data-stu-id="57734-122">-Content</span></span>
<span data-ttu-id="57734-123">Base 64 kodlanmış XML formatlı içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57734-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="57734-124">Bu cmdlet içeriği unattend.xml dosyasına ekler.</span><span class="sxs-lookup"><span data-stu-id="57734-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="57734-125">XML içeriği 4 KB 'den az olmalıdır ve bu cmdlet 'in eklediği ayarın veya özelliğin kök öğesini içermelidir.</span><span class="sxs-lookup"><span data-stu-id="57734-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="57734-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57734-126">-DefaultProfile</span></span>
<span data-ttu-id="57734-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57734-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57734-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="57734-128">-SettingName</span></span>
<span data-ttu-id="57734-129">İçeriğin uygulandığı ayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57734-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="57734-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="57734-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57734-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="57734-131">FirstLogonCommands</span></span>
- <span data-ttu-id="57734-132">Açmayı</span><span class="sxs-lookup"><span data-stu-id="57734-132">AutoLogon</span></span>

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

### <span data-ttu-id="57734-133">-VM</span><span class="sxs-lookup"><span data-stu-id="57734-133">-VM</span></span>
<span data-ttu-id="57734-134">Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57734-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="57734-135">Sanal makine nesnesi edinmek için [Get-AzVM](./Get-AzVM.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="57734-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="57734-136">[New-AzVMConfig](./New-AzVMConfig.md) cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="57734-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="57734-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57734-137">CommonParameters</span></span>
<span data-ttu-id="57734-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57734-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57734-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57734-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57734-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57734-140">INPUTS</span></span>

### <span data-ttu-id="57734-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57734-141">PSVirtualMachine</span></span>
<span data-ttu-id="57734-142">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="57734-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="57734-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57734-143">OUTPUTS</span></span>

### <span data-ttu-id="57734-144">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57734-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="57734-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57734-145">NOTES</span></span>

## <span data-ttu-id="57734-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57734-146">RELATED LINKS</span></span>

[<span data-ttu-id="57734-147">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="57734-147">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="57734-148">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="57734-148">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="57734-149">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="57734-149">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
