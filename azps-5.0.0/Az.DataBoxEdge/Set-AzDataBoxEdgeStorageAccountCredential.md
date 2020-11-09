---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321105"
---
# <span data-ttu-id="6b804-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6b804-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6b804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b804-102">SYNOPSIS</span></span>
<span data-ttu-id="6b804-103">Cihazın depolama hesabı kimlik bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6b804-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="6b804-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b804-104">SYNTAX</span></span>

### <span data-ttu-id="6b804-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b804-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b804-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6b804-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b804-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b804-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b804-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b804-108">DESCRIPTION</span></span>
<span data-ttu-id="6b804-109">**Set-AzDataBoxEdgeStorageAccountCredential** cmdlet 'ı, veri kutusu Edge aygıtındaki bir depolama hesabına karşılık gelen depolama hesabı kimlik bilgisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b804-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="6b804-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b804-110">EXAMPLES</span></span>

### <span data-ttu-id="6b804-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6b804-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="6b804-112">Bir depolama hesabı için Access tuşlarının döndürülmesini sağlar</span><span class="sxs-lookup"><span data-stu-id="6b804-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="6b804-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b804-113">PARAMETERS</span></span>

### <span data-ttu-id="6b804-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="6b804-114">-AsJob</span></span>
<span data-ttu-id="6b804-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6b804-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b804-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b804-116">-DefaultProfile</span></span>
<span data-ttu-id="6b804-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b804-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b804-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="6b804-118">-DeviceName</span></span>
<span data-ttu-id="6b804-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="6b804-119">Device Name</span></span>

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

### <span data-ttu-id="6b804-120">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="6b804-120">-EncryptionKey</span></span>
<span data-ttu-id="6b804-121">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="6b804-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="6b804-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b804-122">-InputObject</span></span>
<span data-ttu-id="6b804-123">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6b804-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b804-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b804-124">-Name</span></span>
<span data-ttu-id="6b804-125">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="6b804-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b804-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b804-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b804-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6b804-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6b804-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6b804-128">-ResourceId</span></span>
<span data-ttu-id="6b804-129">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6b804-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="6b804-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="6b804-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="6b804-131">depolama hesabı erişim anahtarı sağlayın</span><span class="sxs-lookup"><span data-stu-id="6b804-131">provide storage account access key</span></span>

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

### <span data-ttu-id="6b804-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b804-132">-Confirm</span></span>
<span data-ttu-id="6b804-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b804-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b804-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b804-134">-WhatIf</span></span>
<span data-ttu-id="6b804-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b804-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b804-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b804-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b804-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b804-137">CommonParameters</span></span>
<span data-ttu-id="6b804-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b804-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b804-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b804-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b804-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b804-140">INPUTS</span></span>

### <span data-ttu-id="6b804-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6b804-141">System.String</span></span>

### <span data-ttu-id="6b804-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6b804-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6b804-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b804-143">OUTPUTS</span></span>

### <span data-ttu-id="6b804-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6b804-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6b804-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b804-145">NOTES</span></span>

## <span data-ttu-id="6b804-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b804-146">RELATED LINKS</span></span>
