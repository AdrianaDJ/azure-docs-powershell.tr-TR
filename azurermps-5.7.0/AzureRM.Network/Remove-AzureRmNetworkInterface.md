---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 829dc03dad037b6b1576613ab18d9929a777241e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587520"
---
# <span data-ttu-id="b9c0d-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b9c0d-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="b9c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c0d-103">Ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c0d-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c0d-106">**Remove-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="b9c0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c0d-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c0d-108">Örnek 1: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b9c0d-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="b9c0d-109">Bu komut, kaynak grubundaki ResourceGroup1 NetworkInterface1 ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="b9c0d-110">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="b9c0d-111">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b9c0d-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="b9c0d-112">Bu komut, kaynak grubu ResourceGroup1 tüm ağ arabirimlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="b9c0d-113">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="b9c0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c0d-114">PARAMETERS</span></span>

### <span data-ttu-id="b9c0d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b9c0d-115">-AsJob</span></span>
<span data-ttu-id="b9c0d-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b9c0d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9c0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c0d-117">-DefaultProfile</span></span>
<span data-ttu-id="b9c0d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c0d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b9c0d-119">-Force</span></span>
<span data-ttu-id="b9c0d-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9c0d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c0d-121">-Name</span></span>
<span data-ttu-id="b9c0d-122">Bu cmdlet 'in kaldırdığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9c0d-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b9c0d-123">-PassThru</span></span>
<span data-ttu-id="b9c0d-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9c0d-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9c0d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c0d-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9c0d-127">Bu cmdlet 'in kaldırıldığı ağ arabirimini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9c0d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b9c0d-128">-Confirm</span></span>
<span data-ttu-id="b9c0d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c0d-130">-WhatIf</span></span>
<span data-ttu-id="b9c0d-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c0d-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c0d-133">CommonParameters</span></span>
<span data-ttu-id="b9c0d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c0d-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c0d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c0d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c0d-136">INPUTS</span></span>

### <span data-ttu-id="b9c0d-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b9c0d-137">None</span></span>
<span data-ttu-id="b9c0d-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b9c0d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9c0d-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c0d-139">OUTPUTS</span></span>

## <span data-ttu-id="b9c0d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c0d-140">NOTES</span></span>

## <span data-ttu-id="b9c0d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c0d-141">RELATED LINKS</span></span>

[<span data-ttu-id="b9c0d-142">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="b9c0d-142">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="b9c0d-143">Yeni-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="b9c0d-143">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="b9c0d-144">Set-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="b9c0d-144">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


