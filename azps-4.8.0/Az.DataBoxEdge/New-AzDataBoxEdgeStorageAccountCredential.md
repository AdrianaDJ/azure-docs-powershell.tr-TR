---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268029"
---
# <span data-ttu-id="bf748-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bf748-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bf748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf748-102">SYNOPSIS</span></span>
<span data-ttu-id="bf748-103">Cihazda bir Edge depolama hesabı için yeni kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf748-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="bf748-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf748-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf748-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf748-105">DESCRIPTION</span></span>
<span data-ttu-id="bf748-106">**New-AzDataBoxEdgeStorageAccountCredential** cmdlet 'ı bir veri kutusu uç aygıtı için yeni bir Edge depolama hesabı kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf748-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="bf748-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf748-107">EXAMPLES</span></span>

### <span data-ttu-id="bf748-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf748-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="bf748-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf748-109">PARAMETERS</span></span>

### <span data-ttu-id="bf748-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="bf748-110">-AsJob</span></span>
<span data-ttu-id="bf748-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf748-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf748-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf748-112">-DefaultProfile</span></span>
<span data-ttu-id="bf748-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf748-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf748-114">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="bf748-114">-DeviceName</span></span>
<span data-ttu-id="bf748-115">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="bf748-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf748-116">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="bf748-116">-EncryptionKey</span></span>
<span data-ttu-id="bf748-117">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="bf748-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="bf748-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf748-118">-Name</span></span>
<span data-ttu-id="bf748-119">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="bf748-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf748-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf748-120">-ResourceGroupName</span></span>
<span data-ttu-id="bf748-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bf748-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf748-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="bf748-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="bf748-123">depolama hesabı erişim anahtarı sağlayın</span><span class="sxs-lookup"><span data-stu-id="bf748-123">provide storage account access key</span></span>

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

### <span data-ttu-id="bf748-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bf748-124">-StorageAccountType</span></span>
<span data-ttu-id="bf748-125">Olası depolama erişim türü Generalbir depolama, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="bf748-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf748-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf748-126">-Confirm</span></span>
<span data-ttu-id="bf748-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf748-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf748-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf748-128">-WhatIf</span></span>
<span data-ttu-id="bf748-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf748-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf748-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf748-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf748-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf748-131">CommonParameters</span></span>
<span data-ttu-id="bf748-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf748-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf748-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf748-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf748-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf748-134">INPUTS</span></span>

### <span data-ttu-id="bf748-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bf748-135">None</span></span>

## <span data-ttu-id="bf748-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf748-136">OUTPUTS</span></span>

### <span data-ttu-id="bf748-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bf748-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bf748-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf748-138">NOTES</span></span>

## <span data-ttu-id="bf748-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf748-139">RELATED LINKS</span></span>
