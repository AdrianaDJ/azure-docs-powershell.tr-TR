---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268686"
---
# <span data-ttu-id="4da6d-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4da6d-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="4da6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4da6d-102">SYNOPSIS</span></span>
<span data-ttu-id="4da6d-103">Cihazda bir kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4da6d-103">Removes a user on a device.</span></span>

## <span data-ttu-id="4da6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4da6d-104">SYNTAX</span></span>

### <span data-ttu-id="4da6d-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4da6d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da6d-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4da6d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4da6d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4da6d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da6d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4da6d-108">DESCRIPTION</span></span>
<span data-ttu-id="4da6d-109">**Remove-AzStackEdgeUser** cmdlet 'ı yığın uç cihazında bir kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4da6d-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="4da6d-110">Yalnızca türü kullanıcıların oluşturulması `Share` desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4da6d-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="4da6d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4da6d-111">EXAMPLES</span></span>

### <span data-ttu-id="4da6d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4da6d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="4da6d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4da6d-113">PARAMETERS</span></span>

### <span data-ttu-id="4da6d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="4da6d-114">-AsJob</span></span>
<span data-ttu-id="4da6d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4da6d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4da6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da6d-116">-DefaultProfile</span></span>
<span data-ttu-id="4da6d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4da6d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da6d-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="4da6d-118">-DeviceName</span></span>
<span data-ttu-id="4da6d-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="4da6d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4da6d-120">-InputObject</span></span>
<span data-ttu-id="4da6d-121">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="4da6d-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4da6d-122">-Name</span></span>
<span data-ttu-id="4da6d-123">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="4da6d-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6d-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4da6d-124">-PassThru</span></span>
<span data-ttu-id="4da6d-125">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="4da6d-125">returns true if successful</span></span>

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

### <span data-ttu-id="4da6d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da6d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4da6d-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4da6d-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6d-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4da6d-128">-ResourceId</span></span>
<span data-ttu-id="4da6d-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4da6d-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4da6d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4da6d-130">-Confirm</span></span>
<span data-ttu-id="4da6d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4da6d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da6d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da6d-132">-WhatIf</span></span>
<span data-ttu-id="4da6d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4da6d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4da6d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4da6d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da6d-135">CommonParameters</span></span>
<span data-ttu-id="4da6d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4da6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da6d-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4da6d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da6d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4da6d-138">INPUTS</span></span>

### <span data-ttu-id="4da6d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4da6d-139">System.String</span></span>

### <span data-ttu-id="4da6d-140">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4da6d-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="4da6d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4da6d-141">OUTPUTS</span></span>

### <span data-ttu-id="4da6d-142">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4da6d-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="4da6d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4da6d-143">NOTES</span></span>

## <span data-ttu-id="4da6d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4da6d-144">RELATED LINKS</span></span>
