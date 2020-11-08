---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103894"
---
# <span data-ttu-id="0c2f4-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0c2f4-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0c2f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2f4-103">Cihazın depolama hesabı kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="0c2f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c2f4-104">SYNTAX</span></span>

### <span data-ttu-id="0c2f4-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c2f4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2f4-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0c2f4-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c2f4-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c2f4-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c2f4-108">DESCRIPTION</span></span>
<span data-ttu-id="0c2f4-109">**Set-AzStackEdgeStorageAccountCredential** cmdlet 'ı, yığın uç aygıtındaki bir depolama hesabına karşılık gelen depolama hesabı kimlik bilgisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="0c2f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c2f4-110">EXAMPLES</span></span>

### <span data-ttu-id="0c2f4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c2f4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="0c2f4-112">Bir depolama hesabı için Access tuşlarının döndürülmesini sağlar</span><span class="sxs-lookup"><span data-stu-id="0c2f4-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="0c2f4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c2f4-113">PARAMETERS</span></span>

### <span data-ttu-id="0c2f4-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0c2f4-114">-AsJob</span></span>
<span data-ttu-id="0c2f4-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0c2f4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c2f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2f4-116">-DefaultProfile</span></span>
<span data-ttu-id="0c2f4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c2f4-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="0c2f4-118">-DeviceName</span></span>
<span data-ttu-id="0c2f4-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="0c2f4-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-120">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="0c2f4-120">-EncryptionKey</span></span>
<span data-ttu-id="0c2f4-121">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="0c2f4-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c2f4-122">-InputObject</span></span>
<span data-ttu-id="0c2f4-123">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="0c2f4-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c2f4-124">-Name</span></span>
<span data-ttu-id="0c2f4-125">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="0c2f4-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c2f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c2f4-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0c2f4-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c2f4-128">-ResourceId</span></span>
<span data-ttu-id="0c2f4-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c2f4-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="0c2f4-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="0c2f4-131">depolama hesabı erişim anahtarı sağlayın</span><span class="sxs-lookup"><span data-stu-id="0c2f4-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2f4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c2f4-132">-Confirm</span></span>
<span data-ttu-id="0c2f4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2f4-134">-WhatIf</span></span>
<span data-ttu-id="0c2f4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c2f4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2f4-137">CommonParameters</span></span>
<span data-ttu-id="0c2f4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2f4-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c2f4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2f4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c2f4-140">INPUTS</span></span>

### <span data-ttu-id="0c2f4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0c2f4-141">System.String</span></span>

### <span data-ttu-id="0c2f4-142">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0c2f4-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0c2f4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c2f4-143">OUTPUTS</span></span>

### <span data-ttu-id="0c2f4-144">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0c2f4-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0c2f4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c2f4-145">NOTES</span></span>

## <span data-ttu-id="0c2f4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c2f4-146">RELATED LINKS</span></span>
