---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 403c41de0359f2d857d2c86b772e4af419640f2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935289"
---
# <span data-ttu-id="36ef9-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36ef9-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="36ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="36ef9-103">Ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36ef9-103">Removes a network interface.</span></span>

## <span data-ttu-id="36ef9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36ef9-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ef9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="36ef9-106">**Remove-AzNetworkInterface** cmdlet 'ı bir Azure ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36ef9-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="36ef9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="36ef9-108">Örnek 1: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="36ef9-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="36ef9-109">Bu komut, kaynak grubundaki ResourceGroup1 NetworkInterface1 ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36ef9-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="36ef9-110">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="36ef9-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="36ef9-111">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="36ef9-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="36ef9-112">Bu komut, kaynak grubu ResourceGroup1 tüm ağ arabirimlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36ef9-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="36ef9-113">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="36ef9-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="36ef9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36ef9-114">PARAMETERS</span></span>

### <span data-ttu-id="36ef9-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="36ef9-115">-AsJob</span></span>
<span data-ttu-id="36ef9-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="36ef9-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ef9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ef9-117">-DefaultProfile</span></span>
<span data-ttu-id="36ef9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36ef9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ef9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="36ef9-119">-Force</span></span>
<span data-ttu-id="36ef9-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="36ef9-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ef9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="36ef9-121">-Name</span></span>
<span data-ttu-id="36ef9-122">Bu cmdlet 'in kaldırdığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36ef9-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ef9-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36ef9-123">-PassThru</span></span>
<span data-ttu-id="36ef9-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="36ef9-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36ef9-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="36ef9-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ef9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ef9-126">-ResourceGroupName</span></span>
<span data-ttu-id="36ef9-127">Bu cmdlet 'in kaldırıldığı ağ arabirimini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36ef9-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="36ef9-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="36ef9-128">-Confirm</span></span>
<span data-ttu-id="36ef9-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36ef9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ef9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ef9-130">-WhatIf</span></span>
<span data-ttu-id="36ef9-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36ef9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ef9-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36ef9-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ef9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ef9-133">CommonParameters</span></span>
<span data-ttu-id="36ef9-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36ef9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ef9-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ef9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ef9-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36ef9-136">INPUTS</span></span>

## <span data-ttu-id="36ef9-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36ef9-137">OUTPUTS</span></span>

## <span data-ttu-id="36ef9-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36ef9-138">NOTES</span></span>

## <span data-ttu-id="36ef9-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36ef9-139">RELATED LINKS</span></span>

[<span data-ttu-id="36ef9-140">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36ef9-140">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="36ef9-141">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="36ef9-141">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="36ef9-142">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="36ef9-142">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


