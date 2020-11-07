---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: dff83dbb7183c4f9eaf46e883a92a8e615f9cacc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936745"
---
# <span data-ttu-id="bdebb-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bdebb-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bdebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdebb-102">SYNOPSIS</span></span>
<span data-ttu-id="bdebb-103">Cihazın depolama hesabı kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdebb-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="bdebb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdebb-104">SYNTAX</span></span>

### <span data-ttu-id="bdebb-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bdebb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdebb-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bdebb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdebb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdebb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdebb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdebb-108">DESCRIPTION</span></span>
<span data-ttu-id="bdebb-109">**Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet 'i, bir veri kutusu uç aygıtının depolama hesabı kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdebb-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="bdebb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdebb-110">EXAMPLES</span></span>

### <span data-ttu-id="bdebb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bdebb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="bdebb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdebb-112">PARAMETERS</span></span>

### <span data-ttu-id="bdebb-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="bdebb-113">-AsJob</span></span>
<span data-ttu-id="bdebb-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bdebb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdebb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdebb-115">-DefaultProfile</span></span>
<span data-ttu-id="bdebb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bdebb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdebb-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="bdebb-117">-DeviceName</span></span>
<span data-ttu-id="bdebb-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="bdebb-118">Device Name</span></span>

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

### <span data-ttu-id="bdebb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdebb-119">-InputObject</span></span>
<span data-ttu-id="bdebb-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="bdebb-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdebb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bdebb-121">-Name</span></span>
<span data-ttu-id="bdebb-122">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="bdebb-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="bdebb-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bdebb-123">-PassThru</span></span>
<span data-ttu-id="bdebb-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="bdebb-124">returns true if successful</span></span>

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

### <span data-ttu-id="bdebb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdebb-125">-ResourceGroupName</span></span>
<span data-ttu-id="bdebb-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bdebb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="bdebb-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bdebb-127">-ResourceId</span></span>
<span data-ttu-id="bdebb-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bdebb-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="bdebb-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bdebb-129">-Confirm</span></span>
<span data-ttu-id="bdebb-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bdebb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdebb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdebb-131">-WhatIf</span></span>
<span data-ttu-id="bdebb-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdebb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdebb-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bdebb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdebb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdebb-134">CommonParameters</span></span>
<span data-ttu-id="bdebb-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdebb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdebb-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bdebb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdebb-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdebb-137">INPUTS</span></span>

### <span data-ttu-id="bdebb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bdebb-138">System.String</span></span>

### <span data-ttu-id="bdebb-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bdebb-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bdebb-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdebb-140">OUTPUTS</span></span>

### <span data-ttu-id="bdebb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdebb-141">System.Boolean</span></span>

## <span data-ttu-id="bdebb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdebb-142">NOTES</span></span>

## <span data-ttu-id="bdebb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdebb-143">RELATED LINKS</span></span>
