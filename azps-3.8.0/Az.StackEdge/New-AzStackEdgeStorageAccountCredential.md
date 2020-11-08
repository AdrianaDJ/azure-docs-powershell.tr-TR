---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098537"
---
# <span data-ttu-id="93aa7-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="93aa7-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="93aa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="93aa7-103">Cihazda bir Edge depolama hesabı için yeni kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93aa7-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="93aa7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93aa7-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93aa7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="93aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="93aa7-106">**Yeni-AzStackEdgeStorageAccountCredential** cmdlet 'ı, yığın uç aygıtı için yeni bir Edge depolama hesabı kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93aa7-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="93aa7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93aa7-107">EXAMPLES</span></span>

### <span data-ttu-id="93aa7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="93aa7-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="93aa7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93aa7-109">PARAMETERS</span></span>

### <span data-ttu-id="93aa7-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="93aa7-110">-AsJob</span></span>
<span data-ttu-id="93aa7-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="93aa7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93aa7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93aa7-112">-DefaultProfile</span></span>
<span data-ttu-id="93aa7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93aa7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93aa7-114">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="93aa7-114">-DeviceName</span></span>
<span data-ttu-id="93aa7-115">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="93aa7-115">Device Name</span></span>

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

### <span data-ttu-id="93aa7-116">-Şifrelemetuşu</span><span class="sxs-lookup"><span data-stu-id="93aa7-116">-EncryptionKey</span></span>
<span data-ttu-id="93aa7-117">Edge aygıtının şifreleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="93aa7-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="93aa7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="93aa7-118">-Name</span></span>
<span data-ttu-id="93aa7-119">Kullanılacak depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="93aa7-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93aa7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93aa7-120">-ResourceGroupName</span></span>
<span data-ttu-id="93aa7-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="93aa7-121">Resource Group Name</span></span>

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

### <span data-ttu-id="93aa7-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="93aa7-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="93aa7-123">depolama hesabı erişim anahtarı sağlayın</span><span class="sxs-lookup"><span data-stu-id="93aa7-123">provide storage account access key</span></span>

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

### <span data-ttu-id="93aa7-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="93aa7-124">-StorageAccountType</span></span>
<span data-ttu-id="93aa7-125">Olası depolama erişim türü Generalbir depolama, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="93aa7-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="93aa7-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="93aa7-126">-Confirm</span></span>
<span data-ttu-id="93aa7-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93aa7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93aa7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93aa7-128">-WhatIf</span></span>
<span data-ttu-id="93aa7-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93aa7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93aa7-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93aa7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93aa7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93aa7-131">CommonParameters</span></span>
<span data-ttu-id="93aa7-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93aa7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93aa7-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="93aa7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93aa7-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93aa7-134">INPUTS</span></span>

### <span data-ttu-id="93aa7-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="93aa7-135">None</span></span>

## <span data-ttu-id="93aa7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93aa7-136">OUTPUTS</span></span>

### <span data-ttu-id="93aa7-137">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="93aa7-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="93aa7-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93aa7-138">NOTES</span></span>

## <span data-ttu-id="93aa7-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93aa7-139">RELATED LINKS</span></span>
