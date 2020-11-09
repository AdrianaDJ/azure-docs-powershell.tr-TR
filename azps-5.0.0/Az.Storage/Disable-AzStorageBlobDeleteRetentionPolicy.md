---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322277"
---
# <span data-ttu-id="0432a-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0432a-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="0432a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0432a-102">SYNOPSIS</span></span>
<span data-ttu-id="0432a-103">Azure depolama blob hizmeti için bekletme ilkesini Sil 'i devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="0432a-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0432a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0432a-104">SYNTAX</span></span>

### <span data-ttu-id="0432a-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0432a-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0432a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0432a-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0432a-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="0432a-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0432a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0432a-108">DESCRIPTION</span></span>
<span data-ttu-id="0432a-109">**Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silme işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="0432a-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0432a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0432a-110">EXAMPLES</span></span>

### <span data-ttu-id="0432a-111">Örnek 1: blob hizmeti için bekletme ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="0432a-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="0432a-112">Bu komut, blob hizmeti için bekletme ilkesini silme özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="0432a-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="0432a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0432a-113">PARAMETERS</span></span>

### <span data-ttu-id="0432a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0432a-114">-DefaultProfile</span></span>
<span data-ttu-id="0432a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0432a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0432a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0432a-116">-PassThru</span></span>
<span data-ttu-id="0432a-117">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0432a-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="0432a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0432a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0432a-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0432a-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="0432a-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0432a-120">-ResourceId</span></span>
<span data-ttu-id="0432a-121">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="0432a-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="0432a-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0432a-122">-StorageAccount</span></span>
<span data-ttu-id="0432a-123">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="0432a-123">Storage account object</span></span>

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

### <span data-ttu-id="0432a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0432a-124">-StorageAccountName</span></span>
<span data-ttu-id="0432a-125">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="0432a-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="0432a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="0432a-126">-Confirm</span></span>
<span data-ttu-id="0432a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0432a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0432a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0432a-128">-WhatIf</span></span>
<span data-ttu-id="0432a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0432a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0432a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0432a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0432a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0432a-131">CommonParameters</span></span>
<span data-ttu-id="0432a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0432a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0432a-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0432a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0432a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0432a-134">INPUTS</span></span>

### <span data-ttu-id="0432a-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0432a-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0432a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0432a-136">System.String</span></span>

## <span data-ttu-id="0432a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0432a-137">OUTPUTS</span></span>

### <span data-ttu-id="0432a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0432a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="0432a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0432a-139">NOTES</span></span>

## <span data-ttu-id="0432a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0432a-140">RELATED LINKS</span></span>
