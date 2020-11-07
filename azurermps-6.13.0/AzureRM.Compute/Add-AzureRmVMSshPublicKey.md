---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 571d137e369cc997bce2b5a4f21839e64de8021a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763168"
---
# <span data-ttu-id="62feb-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="62feb-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="62feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62feb-102">SYNOPSIS</span></span>
<span data-ttu-id="62feb-103">Sanal makine için SSH için ortak anahtarlar ekler.</span><span class="sxs-lookup"><span data-stu-id="62feb-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62feb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62feb-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62feb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62feb-105">DESCRIPTION</span></span>
<span data-ttu-id="62feb-106">**Add-AzureRmVMSshPublicKey** cmdlet 'ı, güvenli kabukta (SSH) sanal makineye bağlanmak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="62feb-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="62feb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62feb-107">EXAMPLES</span></span>

### <span data-ttu-id="62feb-108">Örnek 1: sanal makineye ortak anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="62feb-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="62feb-109">İlk komut VirtualMachine07 adındaki sanal makineyi **Get-AzureRmVM** cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="62feb-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="62feb-110">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="62feb-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="62feb-111">İkinci komut, yol parametresinin belirttiği VirtualMachine07 üzerinde ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="62feb-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="62feb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62feb-112">PARAMETERS</span></span>

### <span data-ttu-id="62feb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62feb-113">-DefaultProfile</span></span>
<span data-ttu-id="62feb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62feb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62feb-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="62feb-115">-KeyData</span></span>
<span data-ttu-id="62feb-116">Ortak anahtarın temel 64 kodlamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62feb-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="62feb-117">SSH kullanarak veya bu parametrenin belirttiği anahtarı kullanarak sanal makineye bağlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62feb-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="62feb-118">-Yol</span><span class="sxs-lookup"><span data-stu-id="62feb-118">-Path</span></span>
<span data-ttu-id="62feb-119">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="62feb-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="62feb-120">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="62feb-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="62feb-121">-VM</span><span class="sxs-lookup"><span data-stu-id="62feb-121">-VM</span></span>
<span data-ttu-id="62feb-122">Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62feb-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="62feb-123">Sanal makine nesnesi edinmek için [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="62feb-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="62feb-124">Sanal makine nesnesi oluşturmak için [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62feb-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="62feb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62feb-125">CommonParameters</span></span>
<span data-ttu-id="62feb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62feb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62feb-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62feb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62feb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62feb-128">INPUTS</span></span>

### <span data-ttu-id="62feb-129">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="62feb-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="62feb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="62feb-130">System.String</span></span>

## <span data-ttu-id="62feb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62feb-131">OUTPUTS</span></span>

### <span data-ttu-id="62feb-132">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="62feb-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="62feb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62feb-133">NOTES</span></span>

## <span data-ttu-id="62feb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62feb-134">RELATED LINKS</span></span>

[<span data-ttu-id="62feb-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="62feb-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="62feb-136">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="62feb-136">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
