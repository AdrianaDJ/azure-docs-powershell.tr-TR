---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274081"
---
# <span data-ttu-id="0dd04-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="0dd04-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="0dd04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dd04-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd04-103">Bir Azure Securitypartnersağlayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="0dd04-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="0dd04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0dd04-104">SYNTAX</span></span>

### <span data-ttu-id="0dd04-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dd04-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dd04-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dd04-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dd04-107">Securitypartnerproviderresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0dd04-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd04-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0dd04-108">DESCRIPTION</span></span>
<span data-ttu-id="0dd04-109">**Remove-AzSecurityPartnerProvider** cmdlet 'ı bir Azure securitypartnersağlayıcısını siler</span><span class="sxs-lookup"><span data-stu-id="0dd04-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="0dd04-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0dd04-110">EXAMPLES</span></span>

### <span data-ttu-id="0dd04-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0dd04-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="0dd04-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0dd04-112">PARAMETERS</span></span>

### <span data-ttu-id="0dd04-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="0dd04-113">-AsJob</span></span>
<span data-ttu-id="0dd04-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0dd04-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dd04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd04-115">-DefaultProfile</span></span>
<span data-ttu-id="0dd04-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0dd04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd04-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd04-117">-Force</span></span>
<span data-ttu-id="0dd04-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="0dd04-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0dd04-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0dd04-119">-Name</span></span>
<span data-ttu-id="0dd04-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0dd04-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd04-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0dd04-121">-PassThru</span></span>
<span data-ttu-id="0dd04-122">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0dd04-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="0dd04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd04-123">-ResourceGroupName</span></span>
<span data-ttu-id="0dd04-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0dd04-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd04-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0dd04-125">-ResourceId</span></span>
<span data-ttu-id="0dd04-126">Securitypartnersağlayıcı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0dd04-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd04-127">-Securitypartnersağlayıcı</span><span class="sxs-lookup"><span data-stu-id="0dd04-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="0dd04-128">Securitypartnersağlayıcı giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0dd04-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd04-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="0dd04-129">-Confirm</span></span>
<span data-ttu-id="0dd04-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0dd04-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dd04-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd04-131">-WhatIf</span></span>
<span data-ttu-id="0dd04-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0dd04-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dd04-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0dd04-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dd04-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd04-134">CommonParameters</span></span>
<span data-ttu-id="0dd04-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0dd04-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd04-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0dd04-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd04-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0dd04-137">INPUTS</span></span>

### <span data-ttu-id="0dd04-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0dd04-138">System.String</span></span>

### <span data-ttu-id="0dd04-139">Microsoft. Azure. Commands. Network. model. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="0dd04-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="0dd04-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0dd04-140">OUTPUTS</span></span>

### <span data-ttu-id="0dd04-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0dd04-141">System.Boolean</span></span>

## <span data-ttu-id="0dd04-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0dd04-142">NOTES</span></span>

## <span data-ttu-id="0dd04-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0dd04-143">RELATED LINKS</span></span>
