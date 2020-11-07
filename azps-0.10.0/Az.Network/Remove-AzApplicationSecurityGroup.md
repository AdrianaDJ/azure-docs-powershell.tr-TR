---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935307"
---
# <span data-ttu-id="34f0e-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34f0e-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="34f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="34f0e-103">Uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f0e-103">Removes an application security group.</span></span>

## <span data-ttu-id="34f0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34f0e-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34f0e-105">DESCRIPTION</span></span>
<span data-ttu-id="34f0e-106">**Remove-AzApplicationSecurityGroup** cmdlet 'i uygulama güvenlik grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f0e-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="34f0e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34f0e-107">EXAMPLES</span></span>

### <span data-ttu-id="34f0e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34f0e-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="34f0e-109">Bu komut MyResourceGroup adlı kaynak grubunda MyApplicationSecurityGrouo adlı bir uygulama güvenlik grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="34f0e-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="34f0e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34f0e-110">PARAMETERS</span></span>

### <span data-ttu-id="34f0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f0e-111">-DefaultProfile</span></span>
<span data-ttu-id="34f0e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34f0e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34f0e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="34f0e-113">-Force</span></span>
<span data-ttu-id="34f0e-114">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="34f0e-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="34f0e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="34f0e-115">-Name</span></span>
<span data-ttu-id="34f0e-116">Uygulama güvenlik grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34f0e-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="34f0e-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34f0e-117">-PassThru</span></span>
<span data-ttu-id="34f0e-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="34f0e-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="34f0e-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="34f0e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34f0e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f0e-120">-ResourceGroupName</span></span>
<span data-ttu-id="34f0e-121">Uygulama güvenlik grubunun kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="34f0e-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="34f0e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="34f0e-122">-Confirm</span></span>
<span data-ttu-id="34f0e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34f0e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f0e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f0e-124">-WhatIf</span></span>
<span data-ttu-id="34f0e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34f0e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f0e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34f0e-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f0e-127">CommonParameters</span></span>
<span data-ttu-id="34f0e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34f0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f0e-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f0e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f0e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34f0e-130">INPUTS</span></span>

### <span data-ttu-id="34f0e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="34f0e-131">System.String</span></span>

## <span data-ttu-id="34f0e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34f0e-132">OUTPUTS</span></span>

### <span data-ttu-id="34f0e-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="34f0e-133">System.Object</span></span>

## <span data-ttu-id="34f0e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34f0e-134">NOTES</span></span>

## <span data-ttu-id="34f0e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34f0e-135">RELATED LINKS</span></span>

[<span data-ttu-id="34f0e-136">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34f0e-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="34f0e-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="34f0e-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
