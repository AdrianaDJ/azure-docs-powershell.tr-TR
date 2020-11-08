---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107398"
---
# <span data-ttu-id="cdac8-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-101">New-WAPackVM</span></span>

## <span data-ttu-id="cdac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdac8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdac8-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="cdac8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdac8-104">SYNTAX</span></span>

### <span data-ttu-id="cdac8-105">CreateVMFromTemplate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cdac8-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdac8-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="cdac8-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdac8-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="cdac8-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cdac8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdac8-108">DESCRIPTION</span></span>
<span data-ttu-id="cdac8-109">Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="cdac8-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="cdac8-110">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cdac8-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="cdac8-111">Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="cdac8-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="cdac8-112">**Yeni-WAPackVM** cmdlet 'i sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="cdac8-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdac8-113">EXAMPLES</span></span>

### <span data-ttu-id="cdac8-114">Örnek 1: şablon kullanarak Windows işletim sistemi için sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdac8-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="cdac8-115">İlk komut bir **PSCredential** nesnesi oluşturur ve $Credentials değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="cdac8-116">Cmdlet bir hesap ve parola sorar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="cdac8-117">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cdac8-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="cdac8-118">İkinci komut ContosoTemplate04 adındaki sanal makine şablonunu **Get-WAPackVMTemplate** cmdlet 'ini kullanarak alır ve ardından $Template değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="cdac8-119">Son komutu, $Template değişkeninde depolanan şablona dayalı olarak ContosoV023 adlı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="cdac8-120">Komut *Windows* parametresini belirtir ve bu nedenle sanal makine Windows işletim sisteminin bir sürümünü çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cdac8-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="cdac8-121">Örnek 2: şablon kullanarak Linux işletim sistemi için sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdac8-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="cdac8-122">İlk komut bir **PSCredential** nesnesi oluşturur ve $Credentials değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="cdac8-123">İkinci komut ContosoTemplate19 adındaki sanal makine şablonunu **Get-WAPackVMTemplate** cmdlet 'ini kullanarak alır ve ardından $Template değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="cdac8-124">Son komutu, $Template değişkeninde depolanan şablona dayalı olarak ContosoV028 adlı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="cdac8-125">Komut, *Linux* parametresini belirtir ve bu nedenle sanal makinenin Linux işletim sisteminin bir sürümünü çalıştırması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="cdac8-126">Örnek 3: işletim sistemi diskinden ve boyut profilinden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdac8-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="cdac8-127">İlk komut, **Get-wapackkvmosdisk** cmdlet 'ini kullanarak $OSDisk, contosodee</span><span class="sxs-lookup"><span data-stu-id="cdac8-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="cdac8-128">İkinci komut, **Get-WAPackVMSizeProfile** cmdlet 'ini kullanarak, düz Sizevm adlı boyut profilini alır ve $SizeProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="cdac8-129">Son komutu, $OSDisk depolanan işletim sistemi diskinden ve $SizeProfile depolanan boyut profilinde ContosoV073 adlı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="cdac8-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdac8-130">PARAMETERS</span></span>

### <span data-ttu-id="cdac8-131">-\Administrators Sshkey</span><span class="sxs-lookup"><span data-stu-id="cdac8-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="cdac8-132">Yönetici hesabının güvenli kabuk (SSH) anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="cdac8-133">-Linux</span></span>
<span data-ttu-id="cdac8-134">Cmdlet 'in Linux işletim sistemini çalıştırmak için bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="cdac8-135">-Name</span></span>
<span data-ttu-id="cdac8-136">Sanal makine için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="cdac8-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="cdac8-137">-OSDisk</span></span>
<span data-ttu-id="cdac8-138">Bir işletim sistemi diskini **VirtualHardDisk** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="cdac8-139">İşletim sistemi disketi edinmek için **Get-WAPackVMOSDisk** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cdac8-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="cdac8-140">-ProductKey</span></span>
<span data-ttu-id="cdac8-141">Ürün anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-141">Specifies a product key.</span></span>
<span data-ttu-id="cdac8-142">Ürün anahtarı, ürün lisansını tanımlayan 25 basamaklı bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="cdac8-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="cdac8-143">Sanal makineye veya konağa yüklemeyi planladığınız bir işletim sistemi için ürün anahtarı kullanın.</span><span class="sxs-lookup"><span data-stu-id="cdac8-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="cdac8-144">-Profile</span></span>
<span data-ttu-id="cdac8-145">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cdac8-146">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cdac8-147">-Şablon</span><span class="sxs-lookup"><span data-stu-id="cdac8-147">-Template</span></span>
<span data-ttu-id="cdac8-148">Şablon belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-148">Specifies a template.</span></span>
<span data-ttu-id="cdac8-149">Cmdlet, belirttiğiniz şablona göre bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac8-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="cdac8-150">Şablon nesnesi almak için Get-WAPackVMTemplate cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cdac8-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="cdac8-151">-VMCredential</span></span>
<span data-ttu-id="cdac8-152">Yerel yönetici hesabının kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="cdac8-153">**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cdac8-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="cdac8-154">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cdac8-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="cdac8-155">-VMSizeProfile</span></span>
<span data-ttu-id="cdac8-156">Bir sanal makinenin bir boyut profilini **HardwareProfile** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="cdac8-157">Boyut profili edinmek için **Get-WAPackVMSizeProfile** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cdac8-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="cdac8-158">-VNet</span></span>
<span data-ttu-id="cdac8-159">Sanal ağ belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-159">Specifies a virtual network.</span></span>
<span data-ttu-id="cdac8-160">Cmdlet, sanal makineyi belirttiğiniz sanal ağa bağlar.</span><span class="sxs-lookup"><span data-stu-id="cdac8-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="cdac8-161">Sanal ağ edinmek için **Get-WAPackVNet** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cdac8-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="cdac8-162">-Windows</span></span>
<span data-ttu-id="cdac8-163">Cmdlet 'in Windows işletim sistemini çalıştırmak için bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdac8-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac8-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdac8-164">CommonParameters</span></span>
<span data-ttu-id="cdac8-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdac8-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdac8-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdac8-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdac8-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdac8-167">INPUTS</span></span>

## <span data-ttu-id="cdac8-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdac8-168">OUTPUTS</span></span>

## <span data-ttu-id="cdac8-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdac8-169">NOTES</span></span>

## <span data-ttu-id="cdac8-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdac8-170">RELATED LINKS</span></span>

[<span data-ttu-id="cdac8-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="cdac8-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="cdac8-173">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="cdac8-174">Özgeçmiş-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="cdac8-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="cdac8-176">Başlangıç-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="cdac8-177">Dur-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="cdac8-178">Askıya al-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="cdac8-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="cdac8-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="cdac8-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="cdac8-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="cdac8-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="cdac8-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="cdac8-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


