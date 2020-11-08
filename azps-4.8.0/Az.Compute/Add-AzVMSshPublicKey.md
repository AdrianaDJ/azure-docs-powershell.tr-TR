---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268056"
---
# <span data-ttu-id="5172f-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5172f-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="5172f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5172f-102">SYNOPSIS</span></span>
<span data-ttu-id="5172f-103">Yalnızca VM oluştururken sanal makine için SSH için ortak anahtarlar ekler.</span><span class="sxs-lookup"><span data-stu-id="5172f-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="5172f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5172f-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5172f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5172f-105">DESCRIPTION</span></span>
<span data-ttu-id="5172f-106">**Add-AzVMSshPublicKey** cmdlet 'ı, güvenli kabuk (SSH) üzerinden Linux sanal makinesine bağlanmak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="5172f-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="5172f-107">Bu, VM oluşturulduktan sonra, VM oluşturulduktan sonra Update-AzVM olmadan bu komutu kullanmaya çalışırsanız, hata olmaz, komutu Update-AzVM ile birlikte kullanıyorsanız komut hatası olur.</span><span class="sxs-lookup"><span data-stu-id="5172f-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="5172f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5172f-108">EXAMPLES</span></span>

### <span data-ttu-id="5172f-109">Örnek 1: sanal makineye ortak anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="5172f-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="5172f-110">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="5172f-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="5172f-111">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="5172f-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5172f-112">İkinci komut, yol parametresinin belirttiği VirtualMachine07 üzerinde ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="5172f-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="5172f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5172f-113">PARAMETERS</span></span>

### <span data-ttu-id="5172f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5172f-114">-DefaultProfile</span></span>
<span data-ttu-id="5172f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5172f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5172f-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="5172f-116">-KeyData</span></span>
<span data-ttu-id="5172f-117">Ortak anahtarın temel 64 kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5172f-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="5172f-118">SSH kullanarak veya bu parametrenin belirttiği anahtarı kullanarak Linux sanal makinesine bağlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5172f-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5172f-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="5172f-119">-Path</span></span>
<span data-ttu-id="5172f-120">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5172f-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="5172f-121">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="5172f-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5172f-122">-VM</span><span class="sxs-lookup"><span data-stu-id="5172f-122">-VM</span></span>
<span data-ttu-id="5172f-123">Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5172f-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="5172f-124">Sanal makine nesnesi edinmek için [Get-AzVM](./Get-AzVM.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5172f-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="5172f-125">Sanal makine nesnesi oluşturmak için [New-AzVMConfig](./New-AzVMConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5172f-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5172f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5172f-126">CommonParameters</span></span>
<span data-ttu-id="5172f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5172f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5172f-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5172f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5172f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5172f-129">INPUTS</span></span>

### <span data-ttu-id="5172f-130">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5172f-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5172f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5172f-131">System.String</span></span>

## <span data-ttu-id="5172f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5172f-132">OUTPUTS</span></span>

### <span data-ttu-id="5172f-133">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5172f-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5172f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5172f-134">NOTES</span></span>

## <span data-ttu-id="5172f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5172f-135">RELATED LINKS</span></span>

[<span data-ttu-id="5172f-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5172f-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5172f-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5172f-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
