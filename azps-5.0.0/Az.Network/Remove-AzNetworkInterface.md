---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276397"
---
# <span data-ttu-id="55a6b-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="55a6b-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="55a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="55a6b-103">Ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55a6b-103">Removes a network interface.</span></span>

## <span data-ttu-id="55a6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55a6b-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a6b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="55a6b-106">**Remove-AzNetworkInterface** cmdlet 'ı bir Azure ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55a6b-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="55a6b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="55a6b-108">Örnek 1: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="55a6b-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="55a6b-109">Bu komut, kaynak grubundaki ResourceGroup1 NetworkInterface1 ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55a6b-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="55a6b-110">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="55a6b-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="55a6b-111">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="55a6b-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="55a6b-112">Bu komut, kaynak grubu ResourceGroup1 tüm ağ arabirimlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55a6b-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="55a6b-113">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="55a6b-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="55a6b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55a6b-114">PARAMETERS</span></span>

### <span data-ttu-id="55a6b-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="55a6b-115">-AsJob</span></span>
<span data-ttu-id="55a6b-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="55a6b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a6b-117">-DefaultProfile</span></span>
<span data-ttu-id="55a6b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55a6b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55a6b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="55a6b-119">-Force</span></span>
<span data-ttu-id="55a6b-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="55a6b-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55a6b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="55a6b-121">-Name</span></span>
<span data-ttu-id="55a6b-122">Bu cmdlet 'in kaldırdığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a6b-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a6b-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="55a6b-123">-PassThru</span></span>
<span data-ttu-id="55a6b-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="55a6b-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55a6b-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="55a6b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55a6b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a6b-126">-ResourceGroupName</span></span>
<span data-ttu-id="55a6b-127">Bu cmdlet 'in kaldırıldığı ağ arabirimini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a6b-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a6b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="55a6b-128">-Confirm</span></span>
<span data-ttu-id="55a6b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55a6b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a6b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a6b-130">-WhatIf</span></span>
<span data-ttu-id="55a6b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55a6b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a6b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55a6b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a6b-133">CommonParameters</span></span>
<span data-ttu-id="55a6b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55a6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a6b-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55a6b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a6b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55a6b-136">INPUTS</span></span>

### <span data-ttu-id="55a6b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="55a6b-137">System.String</span></span>

## <span data-ttu-id="55a6b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55a6b-138">OUTPUTS</span></span>

### <span data-ttu-id="55a6b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55a6b-139">System.Boolean</span></span>

## <span data-ttu-id="55a6b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55a6b-140">NOTES</span></span>

## <span data-ttu-id="55a6b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55a6b-141">RELATED LINKS</span></span>

[<span data-ttu-id="55a6b-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="55a6b-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="55a6b-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="55a6b-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="55a6b-144">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="55a6b-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


