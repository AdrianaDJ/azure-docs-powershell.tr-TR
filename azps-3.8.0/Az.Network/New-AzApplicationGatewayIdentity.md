---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104803"
---
# <span data-ttu-id="0ba1b-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="0ba1b-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="0ba1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba1b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba1b-103">Uygulama ağ geçidi için bir Identity nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="0ba1b-104">Bu, kullanıcının atadığı kimlik başvurusunu tutar.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="0ba1b-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ba1b-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ba1b-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ba1b-106">DESCRIPTION</span></span>
<span data-ttu-id="0ba1b-107">**New-Azapplicationgatewayıdentity** cmdlet 'i bir uygulama Ağ Geçidi kimlik nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="0ba1b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ba1b-108">EXAMPLES</span></span>

### <span data-ttu-id="0ba1b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0ba1b-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="0ba1b-110">Bu örnekte, Kullanıcı tarafından atanmış bir kimlik oluşturduk ve bunu uygulama ağ geçidiyle kullanılan Identity nesnesiyle başvuralım.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="0ba1b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ba1b-111">PARAMETERS</span></span>

### <span data-ttu-id="0ba1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba1b-112">-DefaultProfile</span></span>
<span data-ttu-id="0ba1b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba1b-114">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="0ba1b-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="0ba1b-115">Uygulama ağ geçidine atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="0ba1b-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ba1b-116">-Confirm</span></span>
<span data-ttu-id="0ba1b-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ba1b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ba1b-118">-WhatIf</span></span>
<span data-ttu-id="0ba1b-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ba1b-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ba1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba1b-121">CommonParameters</span></span>
<span data-ttu-id="0ba1b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ba1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba1b-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba1b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba1b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ba1b-124">INPUTS</span></span>

### <span data-ttu-id="0ba1b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0ba1b-125">System.String</span></span>

## <span data-ttu-id="0ba1b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ba1b-126">OUTPUTS</span></span>

### <span data-ttu-id="0ba1b-127">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="0ba1b-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="0ba1b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ba1b-128">NOTES</span></span>

## <span data-ttu-id="0ba1b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ba1b-129">RELATED LINKS</span></span>
