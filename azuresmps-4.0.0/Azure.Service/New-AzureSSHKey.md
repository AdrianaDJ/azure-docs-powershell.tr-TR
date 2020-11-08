---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105982"
---
# <span data-ttu-id="f6283-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="f6283-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="f6283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6283-102">SYNOPSIS</span></span>
<span data-ttu-id="f6283-103">Var olan bir sertifikayı yeni Linux tabanlı bir Azure sanal makinelerine eklemek için bir SSH anahtar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6283-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="f6283-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6283-104">SYNTAX</span></span>

### <span data-ttu-id="f6283-105">tuş çifti</span><span class="sxs-lookup"><span data-stu-id="f6283-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f6283-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="f6283-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f6283-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6283-107">DESCRIPTION</span></span>
<span data-ttu-id="f6283-108">**New-AzureSSHKey** cmdlet 'i Azure 'a önceden eklenmiş bir SERTIFIKA Için SSH anahtar nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6283-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="f6283-109">Bu SSH anahtar nesnesi, yeni- **AzureVM** kullanılarak yeni bir sanal makine için yapılandırma nesnesi oluştururken veya New- **Azutalep ickvm** ile yeni bir sanal makine oluştururken **Yeni-AzureProvisioningConfig** tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f6283-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="f6283-110">Sanal makine oluşturma dosyasının bir parçası olarak dahil edildiğinde, belirtilen SSH ortak anahtarını veya anahtar çiftini yeni sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="f6283-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="f6283-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6283-111">EXAMPLES</span></span>

### <span data-ttu-id="f6283-112">Örnek 1: sertifika ayar nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6283-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="f6283-113">Bu komut, var olan sertifika için bir sertifika ayarı nesnesi oluşturur ve ardından nesneyi daha sonra kullanmak üzere bir değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="f6283-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="f6283-114">Örnek 2: hizmete sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="f6283-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="f6283-115">Bu komut bir Azure hizmetine sertifika ekler ve ardından sertifikayı kullanan yeni bir Linux sanal makinesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6283-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="f6283-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6283-116">PARAMETERS</span></span>

### <span data-ttu-id="f6283-117">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="f6283-117">-Fingerprint</span></span>
<span data-ttu-id="f6283-118">Sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-118">Specifies the fingerprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6283-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f6283-119">-InformationAction</span></span>
<span data-ttu-id="f6283-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f6283-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f6283-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6283-122">'A</span><span class="sxs-lookup"><span data-stu-id="f6283-122">Continue</span></span>
- <span data-ttu-id="f6283-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="f6283-123">Ignore</span></span>
- <span data-ttu-id="f6283-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f6283-124">Inquire</span></span>
- <span data-ttu-id="f6283-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f6283-125">SilentlyContinue</span></span>
- <span data-ttu-id="f6283-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f6283-126">Stop</span></span>
- <span data-ttu-id="f6283-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f6283-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6283-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f6283-128">-InformationVariable</span></span>
<span data-ttu-id="f6283-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6283-130">-KeyPair</span><span class="sxs-lookup"><span data-stu-id="f6283-130">-KeyPair</span></span>
<span data-ttu-id="f6283-131">Bu cmdlet 'in yeni sanal makine yapılandırmasına SSH anahtar çiftini eklemek için bir nesne oluşturacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6283-132">-Yol</span><span class="sxs-lookup"><span data-stu-id="f6283-132">-Path</span></span>
<span data-ttu-id="f6283-133">SSH ortak anahtarının veya anahtar çiftinin depolanacağı yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6283-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="f6283-134">-PublicKey</span></span>
<span data-ttu-id="f6283-135">Bu cmdlet 'in yeni sanal makine yapılandırmasına SSH ortak anahtarı eklemek için bir nesne oluşturacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6283-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6283-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6283-136">CommonParameters</span></span>
<span data-ttu-id="f6283-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6283-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6283-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6283-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6283-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6283-139">INPUTS</span></span>

## <span data-ttu-id="f6283-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6283-140">OUTPUTS</span></span>

## <span data-ttu-id="f6283-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6283-141">NOTES</span></span>

## <span data-ttu-id="f6283-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6283-142">RELATED LINKS</span></span>

[<span data-ttu-id="f6283-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="f6283-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="f6283-144">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="f6283-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="f6283-145">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f6283-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="f6283-146">Yeni-Azutalep Ickvm</span><span class="sxs-lookup"><span data-stu-id="f6283-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


