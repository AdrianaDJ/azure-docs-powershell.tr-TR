---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586886"
---
# <span data-ttu-id="d56b1-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d56b1-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="d56b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d56b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d56b1-103">Ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56b1-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d56b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d56b1-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d56b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d56b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d56b1-106">**Remove-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56b1-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="d56b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d56b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d56b1-108">Örnek 1: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d56b1-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="d56b1-109">Bu komut, kaynak grubundaki ResourceGroup1 NetworkInterface1 ağ arabirimini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56b1-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d56b1-110">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="d56b1-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="d56b1-111">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d56b1-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="d56b1-112">Bu komut, kaynak grubu ResourceGroup1 tüm ağ arabirimlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d56b1-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d56b1-113">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="d56b1-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="d56b1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d56b1-114">PARAMETERS</span></span>

### <span data-ttu-id="d56b1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d56b1-115">-Force</span></span>
<span data-ttu-id="d56b1-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d56b1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d56b1-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d56b1-117">-Name</span></span>
<span data-ttu-id="d56b1-118">Bu cmdlet 'in kaldırdığı ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56b1-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d56b1-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d56b1-119">-PassThru</span></span>
<span data-ttu-id="d56b1-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d56b1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d56b1-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d56b1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d56b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="d56b1-123">Bu cmdlet 'in kaldırıldığı ağ arabirimini içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d56b1-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d56b1-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d56b1-124">-Confirm</span></span>
<span data-ttu-id="d56b1-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d56b1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56b1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56b1-126">-WhatIf</span></span>
<span data-ttu-id="d56b1-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d56b1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56b1-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d56b1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56b1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56b1-129">-DefaultProfile</span></span>
<span data-ttu-id="d56b1-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d56b1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d56b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56b1-131">CommonParameters</span></span>
<span data-ttu-id="d56b1-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d56b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56b1-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56b1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56b1-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d56b1-134">INPUTS</span></span>

## <span data-ttu-id="d56b1-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d56b1-135">OUTPUTS</span></span>

## <span data-ttu-id="d56b1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d56b1-136">NOTES</span></span>

## <span data-ttu-id="d56b1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d56b1-137">RELATED LINKS</span></span>

[<span data-ttu-id="d56b1-138">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d56b1-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="d56b1-139">Yeni-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d56b1-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="d56b1-140">Set-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d56b1-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


