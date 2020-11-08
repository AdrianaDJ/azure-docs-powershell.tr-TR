---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104557"
---
# <span data-ttu-id="0079e-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="0079e-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="0079e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0079e-102">SYNOPSIS</span></span>
<span data-ttu-id="0079e-103">Cihazda bir kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0079e-103">Removes a user on a device.</span></span>

## <span data-ttu-id="0079e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0079e-104">SYNTAX</span></span>

### <span data-ttu-id="0079e-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0079e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0079e-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0079e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0079e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0079e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0079e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0079e-108">DESCRIPTION</span></span>
<span data-ttu-id="0079e-109">**Remove-AzDataBoxEdgeUser** cmdlet 'ı, veri kutusu Edge aygıtındaki bir kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0079e-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="0079e-110">Yalnızca türü kullanıcıların oluşturulması `Share` desteklenir.</span><span class="sxs-lookup"><span data-stu-id="0079e-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="0079e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0079e-111">EXAMPLES</span></span>

### <span data-ttu-id="0079e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0079e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="0079e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0079e-113">PARAMETERS</span></span>

### <span data-ttu-id="0079e-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0079e-114">-AsJob</span></span>
<span data-ttu-id="0079e-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0079e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0079e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0079e-116">-DefaultProfile</span></span>
<span data-ttu-id="0079e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0079e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0079e-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="0079e-118">-DeviceName</span></span>
<span data-ttu-id="0079e-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="0079e-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0079e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0079e-120">-InputObject</span></span>
<span data-ttu-id="0079e-121">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="0079e-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0079e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0079e-122">-Name</span></span>
<span data-ttu-id="0079e-123">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="0079e-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0079e-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0079e-124">-PassThru</span></span>
<span data-ttu-id="0079e-125">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="0079e-125">returns true if successful</span></span>

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

### <span data-ttu-id="0079e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0079e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0079e-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0079e-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0079e-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0079e-128">-ResourceId</span></span>
<span data-ttu-id="0079e-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0079e-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="0079e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0079e-130">-Confirm</span></span>
<span data-ttu-id="0079e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0079e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0079e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0079e-132">-WhatIf</span></span>
<span data-ttu-id="0079e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0079e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0079e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0079e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0079e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0079e-135">CommonParameters</span></span>
<span data-ttu-id="0079e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0079e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0079e-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0079e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0079e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0079e-138">INPUTS</span></span>

### <span data-ttu-id="0079e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0079e-139">System.String</span></span>

### <span data-ttu-id="0079e-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="0079e-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="0079e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0079e-141">OUTPUTS</span></span>

### <span data-ttu-id="0079e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0079e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0079e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0079e-143">NOTES</span></span>

## <span data-ttu-id="0079e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0079e-144">RELATED LINKS</span></span>
