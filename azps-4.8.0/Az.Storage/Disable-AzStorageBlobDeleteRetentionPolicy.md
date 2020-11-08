---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110214"
---
# <span data-ttu-id="df44a-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="df44a-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="df44a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df44a-102">SYNOPSIS</span></span>
<span data-ttu-id="df44a-103">Azure depolama blob hizmeti için bekletme ilkesini Sil 'i devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="df44a-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="df44a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df44a-104">SYNTAX</span></span>

### <span data-ttu-id="df44a-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df44a-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df44a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="df44a-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df44a-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="df44a-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df44a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="df44a-108">DESCRIPTION</span></span>
<span data-ttu-id="df44a-109">**Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silme işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="df44a-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="df44a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df44a-110">EXAMPLES</span></span>

### <span data-ttu-id="df44a-111">Örnek 1: blob hizmeti için bekletme ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="df44a-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="df44a-112">Bu komut, blob hizmeti için bekletme ilkesini silme özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="df44a-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="df44a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df44a-113">PARAMETERS</span></span>

### <span data-ttu-id="df44a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df44a-114">-DefaultProfile</span></span>
<span data-ttu-id="df44a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df44a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df44a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="df44a-116">-PassThru</span></span>
<span data-ttu-id="df44a-117">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="df44a-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="df44a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df44a-118">-ResourceGroupName</span></span>
<span data-ttu-id="df44a-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="df44a-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="df44a-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="df44a-120">-ResourceId</span></span>
<span data-ttu-id="df44a-121">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="df44a-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="df44a-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="df44a-122">-StorageAccount</span></span>
<span data-ttu-id="df44a-123">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="df44a-123">Storage account object</span></span>

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

### <span data-ttu-id="df44a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="df44a-124">-StorageAccountName</span></span>
<span data-ttu-id="df44a-125">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="df44a-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="df44a-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="df44a-126">-Confirm</span></span>
<span data-ttu-id="df44a-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df44a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df44a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df44a-128">-WhatIf</span></span>
<span data-ttu-id="df44a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df44a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df44a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df44a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df44a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df44a-131">CommonParameters</span></span>
<span data-ttu-id="df44a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df44a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df44a-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df44a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df44a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df44a-134">INPUTS</span></span>

### <span data-ttu-id="df44a-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="df44a-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="df44a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="df44a-136">System.String</span></span>

## <span data-ttu-id="df44a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df44a-137">OUTPUTS</span></span>

### <span data-ttu-id="df44a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="df44a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="df44a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df44a-139">NOTES</span></span>

## <span data-ttu-id="df44a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df44a-140">RELATED LINKS</span></span>
