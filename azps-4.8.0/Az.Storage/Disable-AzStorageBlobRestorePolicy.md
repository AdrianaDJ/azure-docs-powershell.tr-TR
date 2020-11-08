---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110205"
---
# <span data-ttu-id="ce4dc-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="ce4dc-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="ce4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4dc-103">Depolama hesabında blob geri yükleme Ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="ce4dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce4dc-104">SYNTAX</span></span>

### <span data-ttu-id="ce4dc-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce4dc-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce4dc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ce4dc-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce4dc-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="ce4dc-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce4dc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce4dc-108">DESCRIPTION</span></span>
<span data-ttu-id="ce4dc-109">**Disable-AzStorageBlobRestorePolicy** cmdlet 'ı, Azure depolama blob hizmeti Için blob geri yükleme ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="ce4dc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce4dc-110">EXAMPLES</span></span>

### <span data-ttu-id="ce4dc-111">Örnek 1: depolama hesabında Azure depolama blob hizmeti için blob geri yükleme Ilkesini devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="ce4dc-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="ce4dc-112">Bu komut, depolama hesabında Azure depolama blob hizmeti için blob geri yükleme Ilkesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="ce4dc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce4dc-113">PARAMETERS</span></span>

### <span data-ttu-id="ce4dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4dc-114">-DefaultProfile</span></span>
<span data-ttu-id="ce4dc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce4dc-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ce4dc-116">-PassThru</span></span>
<span data-ttu-id="ce4dc-117">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ce4dc-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="ce4dc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce4dc-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce4dc-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4dc-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ce4dc-120">-ResourceId</span></span>
<span data-ttu-id="ce4dc-121">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4dc-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce4dc-122">-StorageAccount</span></span>
<span data-ttu-id="ce4dc-123">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce4dc-123">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4dc-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce4dc-124">-StorageAccountName</span></span>
<span data-ttu-id="ce4dc-125">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4dc-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce4dc-126">-Confirm</span></span>
<span data-ttu-id="ce4dc-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce4dc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce4dc-128">-WhatIf</span></span>
<span data-ttu-id="ce4dc-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce4dc-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce4dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4dc-131">CommonParameters</span></span>
<span data-ttu-id="ce4dc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce4dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4dc-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce4dc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4dc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce4dc-134">INPUTS</span></span>

### <span data-ttu-id="ce4dc-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce4dc-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ce4dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ce4dc-136">System.String</span></span>

## <span data-ttu-id="ce4dc-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce4dc-137">OUTPUTS</span></span>

### <span data-ttu-id="ce4dc-138">Microsoft. Azure. Commands. Management. Storage. model. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="ce4dc-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="ce4dc-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce4dc-139">NOTES</span></span>

## <span data-ttu-id="ce4dc-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce4dc-140">RELATED LINKS</span></span>
