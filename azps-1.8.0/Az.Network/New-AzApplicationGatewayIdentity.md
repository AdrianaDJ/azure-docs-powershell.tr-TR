---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 3bb2df6349c734e9802183c13eb39ae8ceafc50b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760403"
---
# <span data-ttu-id="6faf8-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="6faf8-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="6faf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6faf8-102">SYNOPSIS</span></span>
<span data-ttu-id="6faf8-103">Uygulama ağ geçidi için bir Identity nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6faf8-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="6faf8-104">Bu, kullanıcının atadığı kimlik başvurusunu tutar.</span><span class="sxs-lookup"><span data-stu-id="6faf8-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="6faf8-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6faf8-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6faf8-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="6faf8-106">DESCRIPTION</span></span>
<span data-ttu-id="6faf8-107">**New-Azapplicationgatewayıdentity** cmdlet 'i bir uygulama Ağ Geçidi kimlik nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6faf8-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="6faf8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6faf8-108">EXAMPLES</span></span>

### <span data-ttu-id="6faf8-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6faf8-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="6faf8-110">Bu örnekte, Kullanıcı tarafından atanmış bir kimlik oluşturduk ve bunu uygulama ağ geçidiyle kullanılan Identity nesnesiyle başvuralım.</span><span class="sxs-lookup"><span data-stu-id="6faf8-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="6faf8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6faf8-111">PARAMETERS</span></span>

### <span data-ttu-id="6faf8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6faf8-112">-DefaultProfile</span></span>
<span data-ttu-id="6faf8-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6faf8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6faf8-114">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="6faf8-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="6faf8-115">Uygulama ağ geçidine atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="6faf8-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6faf8-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="6faf8-116">-Confirm</span></span>
<span data-ttu-id="6faf8-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6faf8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6faf8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6faf8-118">-WhatIf</span></span>
<span data-ttu-id="6faf8-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6faf8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6faf8-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6faf8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6faf8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6faf8-121">CommonParameters</span></span>
<span data-ttu-id="6faf8-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6faf8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6faf8-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6faf8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6faf8-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6faf8-124">INPUTS</span></span>

### <span data-ttu-id="6faf8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6faf8-125">System.String</span></span>

## <span data-ttu-id="6faf8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6faf8-126">OUTPUTS</span></span>

### <span data-ttu-id="6faf8-127">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="6faf8-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="6faf8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6faf8-128">NOTES</span></span>

## <span data-ttu-id="6faf8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6faf8-129">RELATED LINKS</span></span>
