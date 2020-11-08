---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105955"
---
# <span data-ttu-id="ebe71-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ebe71-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="ebe71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe71-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe71-103">Azure sanal makinesine ortak IP ekler.</span><span class="sxs-lookup"><span data-stu-id="ebe71-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="ebe71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebe71-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ebe71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebe71-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe71-106">**Set-AzurePublicIP** cmdlet 'ı bir Azure sanal MAKINESINE ortak IP ekler.</span><span class="sxs-lookup"><span data-stu-id="ebe71-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="ebe71-107">Var olan bir sanal makine için bu cmdlet 'i çalıştırırsanız, değişikliklerinizi uygulamak için sanal makineyi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="ebe71-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="ebe71-108">Genel IP için bir etki alanı adı etiketi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ebe71-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="ebe71-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebe71-109">EXAMPLES</span></span>

### <span data-ttu-id="ebe71-110">Örnek 1: var olan bir sanal makineye ortak IP ekleme</span><span class="sxs-lookup"><span data-stu-id="ebe71-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="ebe71-111">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak Ftpınazure adlı hizmette ftpınstance adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="ebe71-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ebe71-112">Komut, ardışık düzen işlecini kullanarak bu sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebe71-113">Current cmdlet 'i, genel IP adı ftpıp adını ekler.</span><span class="sxs-lookup"><span data-stu-id="ebe71-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ebe71-114">Komut, sanal makineyi değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="ebe71-115">Örnek 2: yeni bir sanal makineye ortak IP ekleme</span><span class="sxs-lookup"><span data-stu-id="ebe71-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ebe71-116">Bu komut, **New-AzureVMConfig** cmdlet 'ini kullanarak bir sanal makine yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ebe71-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="ebe71-117">Komut bu nesneyi ek yapılandırma sağlayan **Add-AzureProvisioningConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="ebe71-118">Current cmdlet 'i, genel IP adı ftpıp adını ekler.</span><span class="sxs-lookup"><span data-stu-id="ebe71-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ebe71-119">Komut, yapılandırmayı sanal makineyi oluşturan **New-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="ebe71-120">Örnek 3: var olan bir sanal makineye ortak IP ve etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="ebe71-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="ebe71-121">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak Ftpınazure adlı hizmette ftpınstance adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="ebe71-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ebe71-122">Komut, ardışık düzen işlecini kullanarak bu sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebe71-123">Geçerli cmdlet, Public IP Name ftpıp adını ve adName etiketini ekler.</span><span class="sxs-lookup"><span data-stu-id="ebe71-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ebe71-124">Komut değişikliklerinizi uygulayan sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="ebe71-125">Örnek 4: yeni bir sanal makineye ortak IP ve etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="ebe71-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ebe71-126">Bu komut, bir sanal makine yapılandırma nesnesi oluşturur ve bu nesneyi ek yapılandırma sağlayan **Add-AzureProvisioningConfig** ile geçirir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="ebe71-127">Geçerli cmdlet, Public IP Name ftpıp adını ve adName etiketini ekler.</span><span class="sxs-lookup"><span data-stu-id="ebe71-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ebe71-128">Bu komut sanal makineyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ebe71-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="ebe71-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebe71-129">PARAMETERS</span></span>

### <span data-ttu-id="ebe71-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ebe71-130">-DomainNameLabel</span></span>
<span data-ttu-id="ebe71-131">Genel IP adresi için karşılık gelen DNS girdisinde kullanılacak adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe71-132">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="ebe71-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ebe71-133">TCP boşta kalma zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe71-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ebe71-134">-InformationAction</span></span>
<span data-ttu-id="ebe71-135">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ebe71-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ebe71-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ebe71-137">'A</span><span class="sxs-lookup"><span data-stu-id="ebe71-137">Continue</span></span>
- <span data-ttu-id="ebe71-138">Manıza</span><span class="sxs-lookup"><span data-stu-id="ebe71-138">Ignore</span></span>
- <span data-ttu-id="ebe71-139">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ebe71-139">Inquire</span></span>
- <span data-ttu-id="ebe71-140">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ebe71-140">SilentlyContinue</span></span>
- <span data-ttu-id="ebe71-141">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ebe71-141">Stop</span></span>
- <span data-ttu-id="ebe71-142">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ebe71-142">Suspend</span></span>

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

### <span data-ttu-id="ebe71-143">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ebe71-143">-InformationVariable</span></span>
<span data-ttu-id="ebe71-144">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ebe71-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="ebe71-145">-Profile</span></span>
<span data-ttu-id="ebe71-146">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebe71-147">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ebe71-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ebe71-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="ebe71-148">-PublicIPName</span></span>
<span data-ttu-id="ebe71-149">Genel IP adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-149">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="ebe71-150">-VM</span><span class="sxs-lookup"><span data-stu-id="ebe71-150">-VM</span></span>
<span data-ttu-id="ebe71-151">Bu cmdlet 'in genel IP 'yi eklediği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebe71-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe71-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe71-152">CommonParameters</span></span>
<span data-ttu-id="ebe71-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebe71-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe71-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe71-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe71-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebe71-155">INPUTS</span></span>

## <span data-ttu-id="ebe71-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebe71-156">OUTPUTS</span></span>

### <span data-ttu-id="ebe71-157">Microsoft. Windowsaziy. Commands. ServiceManagement. model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="ebe71-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="ebe71-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebe71-158">NOTES</span></span>

## <span data-ttu-id="ebe71-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebe71-159">RELATED LINKS</span></span>

[<span data-ttu-id="ebe71-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ebe71-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="ebe71-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ebe71-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ebe71-162">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ebe71-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ebe71-163">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ebe71-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ebe71-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ebe71-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="ebe71-165">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ebe71-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


