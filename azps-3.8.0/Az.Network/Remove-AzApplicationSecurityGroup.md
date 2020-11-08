---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104084"
---
# <span data-ttu-id="873f5-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="873f5-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="873f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="873f5-102">SYNOPSIS</span></span>
<span data-ttu-id="873f5-103">Uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="873f5-103">Removes an application security group.</span></span>

## <span data-ttu-id="873f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="873f5-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="873f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="873f5-105">DESCRIPTION</span></span>
<span data-ttu-id="873f5-106">**Remove-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="873f5-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="873f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="873f5-107">EXAMPLES</span></span>

### <span data-ttu-id="873f5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="873f5-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="873f5-109">Bu komut MyResourceGroup adlı kaynak grubunda MyApplicationSecurityGrouo adlı bir uygulama güvenlik grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="873f5-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="873f5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="873f5-110">PARAMETERS</span></span>

### <span data-ttu-id="873f5-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="873f5-111">-AsJob</span></span>
<span data-ttu-id="873f5-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="873f5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="873f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873f5-113">-DefaultProfile</span></span>
<span data-ttu-id="873f5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="873f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="873f5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="873f5-115">-Force</span></span>
<span data-ttu-id="873f5-116">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="873f5-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="873f5-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="873f5-117">-Name</span></span>
<span data-ttu-id="873f5-118">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="873f5-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="873f5-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="873f5-119">-PassThru</span></span>
<span data-ttu-id="873f5-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="873f5-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="873f5-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="873f5-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="873f5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873f5-122">-ResourceGroupName</span></span>
<span data-ttu-id="873f5-123">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="873f5-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="873f5-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="873f5-124">-Confirm</span></span>
<span data-ttu-id="873f5-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="873f5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="873f5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="873f5-126">-WhatIf</span></span>
<span data-ttu-id="873f5-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="873f5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="873f5-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="873f5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="873f5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873f5-129">CommonParameters</span></span>
<span data-ttu-id="873f5-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="873f5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873f5-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="873f5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873f5-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="873f5-132">INPUTS</span></span>

### <span data-ttu-id="873f5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="873f5-133">System.String</span></span>

## <span data-ttu-id="873f5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="873f5-134">OUTPUTS</span></span>

### <span data-ttu-id="873f5-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="873f5-135">System.Boolean</span></span>

## <span data-ttu-id="873f5-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="873f5-136">NOTES</span></span>

## <span data-ttu-id="873f5-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="873f5-137">RELATED LINKS</span></span>

[<span data-ttu-id="873f5-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="873f5-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="873f5-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="873f5-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
