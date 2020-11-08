---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266751"
---
# <span data-ttu-id="3d910-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d910-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="3d910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d910-102">SYNOPSIS</span></span>
<span data-ttu-id="3d910-103">Cihazda yeni bir Edge depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d910-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="3d910-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d910-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d910-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d910-105">DESCRIPTION</span></span>
<span data-ttu-id="3d910-106">**Yeni-AzStackEdgeStorageAccount** cmdlet 'ı, yığın uç cihazında yeni bir Edge depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d910-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="3d910-107">Bir cihazda, tek bir kenar depolama hesabı yalnızca bir bulut depolama hesabına eşleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3d910-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="3d910-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d910-108">EXAMPLES</span></span>

### <span data-ttu-id="3d910-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d910-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="3d910-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3d910-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="3d910-111">cihazda 2 ' den fazla bulut depolama hesabını paylaşamaz</span><span class="sxs-lookup"><span data-stu-id="3d910-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="3d910-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d910-112">PARAMETERS</span></span>

### <span data-ttu-id="3d910-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="3d910-113">-AsJob</span></span>
<span data-ttu-id="3d910-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3d910-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d910-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="3d910-115">-Cloud</span></span>
<span data-ttu-id="3d910-116">Bir Cloudiçin bir CloudStorageAccount kullanacak</span><span class="sxs-lookup"><span data-stu-id="3d910-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d910-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d910-117">-DefaultProfile</span></span>
<span data-ttu-id="3d910-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d910-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d910-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="3d910-119">-DeviceName</span></span>
<span data-ttu-id="3d910-120">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="3d910-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d910-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d910-121">-Name</span></span>
<span data-ttu-id="3d910-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="3d910-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d910-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d910-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d910-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3d910-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d910-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="3d910-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="3d910-126">Var olan StorageAccountCredential 'in kaynak adını sağlayın</span><span class="sxs-lookup"><span data-stu-id="3d910-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="3d910-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d910-127">-Confirm</span></span>
<span data-ttu-id="3d910-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d910-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d910-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d910-129">-WhatIf</span></span>
<span data-ttu-id="3d910-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d910-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d910-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d910-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d910-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d910-132">CommonParameters</span></span>
<span data-ttu-id="3d910-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d910-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d910-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d910-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d910-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d910-135">INPUTS</span></span>

### <span data-ttu-id="3d910-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3d910-136">System.String</span></span>

### <span data-ttu-id="3d910-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d910-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d910-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d910-138">OUTPUTS</span></span>

### <span data-ttu-id="3d910-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d910-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="3d910-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d910-140">NOTES</span></span>

## <span data-ttu-id="3d910-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d910-141">RELATED LINKS</span></span>
