---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592240"
---
# <span data-ttu-id="16a0a-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="16a0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="16a0a-103">Bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="16a0a-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16a0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16a0a-104">SYNTAX</span></span>

### <span data-ttu-id="16a0a-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16a0a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16a0a-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="16a0a-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16a0a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="16a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="16a0a-108">**Stop-AzureRmVM** cmdlet 'ı bir Azure sanal makinesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="16a0a-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="16a0a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16a0a-109">EXAMPLES</span></span>

### <span data-ttu-id="16a0a-110">Örnek 1: sanal makineyi durdurma</span><span class="sxs-lookup"><span data-stu-id="16a0a-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="16a0a-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makineyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="16a0a-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="16a0a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16a0a-112">PARAMETERS</span></span>

### <span data-ttu-id="16a0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a0a-113">-DefaultProfile</span></span>
<span data-ttu-id="16a0a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16a0a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16a0a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="16a0a-115">-Force</span></span>
<span data-ttu-id="16a0a-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="16a0a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="16a0a-117">-Id</span></span>
<span data-ttu-id="16a0a-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16a0a-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="16a0a-119">-Name</span></span>
<span data-ttu-id="16a0a-120">Sanal makine adı.</span><span class="sxs-lookup"><span data-stu-id="16a0a-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a0a-121">-ResourceGroupName</span></span>
<span data-ttu-id="16a0a-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16a0a-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-123">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="16a0a-123">-StayProvisioned</span></span>
<span data-ttu-id="16a0a-124">Cmdlet, VMSS içindeki tüm sanal makineleri durdurur ancak bunları serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="16a0a-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="16a0a-125">Hesap, durdurulan sanal makineler için ücretlendirilecek.</span><span class="sxs-lookup"><span data-stu-id="16a0a-125">The account is charged for the stopped virtual machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="16a0a-126">-Confirm</span></span>
<span data-ttu-id="16a0a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16a0a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16a0a-128">-WhatIf</span></span>
<span data-ttu-id="16a0a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16a0a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16a0a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16a0a-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16a0a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a0a-131">CommonParameters</span></span>
<span data-ttu-id="16a0a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16a0a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a0a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16a0a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a0a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16a0a-134">INPUTS</span></span>

## <span data-ttu-id="16a0a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16a0a-135">OUTPUTS</span></span>

## <span data-ttu-id="16a0a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16a0a-136">NOTES</span></span>

## <span data-ttu-id="16a0a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16a0a-137">RELATED LINKS</span></span>

[<span data-ttu-id="16a0a-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="16a0a-139">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="16a0a-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="16a0a-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="16a0a-142">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="16a0a-143">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="16a0a-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


