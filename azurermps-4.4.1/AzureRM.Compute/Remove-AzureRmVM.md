---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592638"
---
# <span data-ttu-id="b35e9-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="b35e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b35e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b35e9-103">Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b35e9-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b35e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b35e9-104">SYNTAX</span></span>

### <span data-ttu-id="b35e9-105">ResourceGroupNameParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b35e9-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b35e9-106">Idparametersetname</span><span class="sxs-lookup"><span data-stu-id="b35e9-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b35e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b35e9-107">DESCRIPTION</span></span>
<span data-ttu-id="b35e9-108">**Remove-AzureRmVM** cmdlet 'i Azure 'dan bir sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b35e9-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="b35e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b35e9-109">EXAMPLES</span></span>

### <span data-ttu-id="b35e9-110">Örnek 1: sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="b35e9-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b35e9-111">Bu komut, kaynak grubundaki VirtualMachine07 adındaki sanal makineyi kaldırır ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b35e9-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="b35e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b35e9-112">PARAMETERS</span></span>

### <span data-ttu-id="b35e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35e9-113">-DefaultProfile</span></span>
<span data-ttu-id="b35e9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b35e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b35e9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b35e9-115">-Force</span></span>
<span data-ttu-id="b35e9-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b35e9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35e9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b35e9-117">-Id</span></span>
<span data-ttu-id="b35e9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b35e9-118">The resource group name.</span></span>

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

### <span data-ttu-id="b35e9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b35e9-119">-Name</span></span>
<span data-ttu-id="b35e9-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b35e9-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b35e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="b35e9-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b35e9-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b35e9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b35e9-123">-Confirm</span></span>
<span data-ttu-id="b35e9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b35e9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35e9-125">-WhatIf</span></span>
<span data-ttu-id="b35e9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b35e9-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b35e9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b35e9-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35e9-128">CommonParameters</span></span>
<span data-ttu-id="b35e9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b35e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35e9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b35e9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35e9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b35e9-131">INPUTS</span></span>

## <span data-ttu-id="b35e9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b35e9-132">OUTPUTS</span></span>

## <span data-ttu-id="b35e9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b35e9-133">NOTES</span></span>

## <span data-ttu-id="b35e9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b35e9-134">RELATED LINKS</span></span>

[<span data-ttu-id="b35e9-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b35e9-136">Yeni-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b35e9-137">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b35e9-138">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b35e9-139">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b35e9-140">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b35e9-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


