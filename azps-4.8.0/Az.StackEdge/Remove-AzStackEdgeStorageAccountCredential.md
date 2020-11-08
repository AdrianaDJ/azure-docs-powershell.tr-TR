---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268689"
---
# <span data-ttu-id="18a17-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="18a17-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="18a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18a17-102">SYNOPSIS</span></span>
<span data-ttu-id="18a17-103">Cihazın depolama hesabı kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18a17-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="18a17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18a17-104">SYNTAX</span></span>

### <span data-ttu-id="18a17-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18a17-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18a17-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="18a17-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a17-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a17-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a17-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="18a17-108">DESCRIPTION</span></span>
<span data-ttu-id="18a17-109">**Remove-AzStackEdgeStorageAccountCredential** cmdlet 'ı, yığın uç aygıtının depolama hesabı kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18a17-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="18a17-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18a17-110">EXAMPLES</span></span>

### <span data-ttu-id="18a17-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18a17-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="18a17-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18a17-112">PARAMETERS</span></span>

### <span data-ttu-id="18a17-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="18a17-113">-AsJob</span></span>
<span data-ttu-id="18a17-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="18a17-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18a17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a17-115">-DefaultProfile</span></span>
<span data-ttu-id="18a17-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18a17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a17-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="18a17-117">-DeviceName</span></span>
<span data-ttu-id="18a17-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="18a17-118">Device Name</span></span>

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

### <span data-ttu-id="18a17-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18a17-119">-InputObject</span></span>
<span data-ttu-id="18a17-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="18a17-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a17-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="18a17-121">-Name</span></span>
<span data-ttu-id="18a17-122">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="18a17-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a17-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="18a17-123">-PassThru</span></span>
<span data-ttu-id="18a17-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="18a17-124">returns true if successful</span></span>

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

### <span data-ttu-id="18a17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a17-125">-ResourceGroupName</span></span>
<span data-ttu-id="18a17-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="18a17-126">Resource Group Name</span></span>

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

### <span data-ttu-id="18a17-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="18a17-127">-ResourceId</span></span>
<span data-ttu-id="18a17-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="18a17-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="18a17-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="18a17-129">-Confirm</span></span>
<span data-ttu-id="18a17-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18a17-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a17-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a17-131">-WhatIf</span></span>
<span data-ttu-id="18a17-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18a17-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18a17-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18a17-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a17-134">CommonParameters</span></span>
<span data-ttu-id="18a17-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18a17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a17-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="18a17-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a17-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18a17-137">INPUTS</span></span>

### <span data-ttu-id="18a17-138">System. String</span><span class="sxs-lookup"><span data-stu-id="18a17-138">System.String</span></span>

### <span data-ttu-id="18a17-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="18a17-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="18a17-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18a17-140">OUTPUTS</span></span>

### <span data-ttu-id="18a17-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18a17-141">System.Boolean</span></span>

## <span data-ttu-id="18a17-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18a17-142">NOTES</span></span>

## <span data-ttu-id="18a17-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18a17-143">RELATED LINKS</span></span>
