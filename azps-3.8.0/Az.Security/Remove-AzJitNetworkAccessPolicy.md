---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 21a31d2d4e094e986ad862bfe69baef98148e5f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097065"
---
# <span data-ttu-id="cdc0d-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc0d-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cdc0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc0d-103">Bir JıT ağ erişim ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="cdc0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdc0d-104">SYNTAX</span></span>

### <span data-ttu-id="cdc0d-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cdc0d-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdc0d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="cdc0d-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdc0d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cdc0d-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc0d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdc0d-108">DESCRIPTION</span></span>
<span data-ttu-id="cdc0d-109">Bir kerelik ağ erişim ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="cdc0d-110">Bu eylemden sonra, Kullanıcı silinen ilke içinde yapılandırılmış VM 'lerde geçici ağ bağlantısı istemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="cdc0d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdc0d-111">EXAMPLES</span></span>

### <span data-ttu-id="cdc0d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cdc0d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="cdc0d-113">Bir kerelik ağ erişim ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="cdc0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdc0d-114">PARAMETERS</span></span>

### <span data-ttu-id="cdc0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc0d-115">-DefaultProfile</span></span>
<span data-ttu-id="cdc0d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc0d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdc0d-117">-InputObject</span></span>
<span data-ttu-id="cdc0d-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc0d-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="cdc0d-119">-Location</span></span>
<span data-ttu-id="cdc0d-120">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc0d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cdc0d-121">-Name</span></span>
<span data-ttu-id="cdc0d-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc0d-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cdc0d-123">-PassThru</span></span>
<span data-ttu-id="cdc0d-124">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="cdc0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdc0d-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc0d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cdc0d-127">-ResourceId</span></span>
<span data-ttu-id="cdc0d-128">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc0d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="cdc0d-129">-Confirm</span></span>
<span data-ttu-id="cdc0d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc0d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc0d-131">-WhatIf</span></span>
<span data-ttu-id="cdc0d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdc0d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc0d-134">CommonParameters</span></span>
<span data-ttu-id="cdc0d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc0d-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc0d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc0d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdc0d-137">INPUTS</span></span>

### <span data-ttu-id="cdc0d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cdc0d-138">System.String</span></span>

### <span data-ttu-id="cdc0d-139">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdc0d-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="cdc0d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdc0d-140">OUTPUTS</span></span>

### <span data-ttu-id="cdc0d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdc0d-141">System.Boolean</span></span>

## <span data-ttu-id="cdc0d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdc0d-142">NOTES</span></span>

## <span data-ttu-id="cdc0d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdc0d-143">RELATED LINKS</span></span>
