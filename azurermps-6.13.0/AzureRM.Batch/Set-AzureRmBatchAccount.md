---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: d67c6b32f26b1addc1cc4ae165f572a3286440cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761985"
---
# <span data-ttu-id="66ec9-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66ec9-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="66ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="66ec9-103">Bir toplu Iş hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66ec9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66ec9-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66ec9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="66ec9-106">**Set-AzureRmBatchAccount** cmdlet 'ı bir Azure toplu hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="66ec9-107">Şu anda bu cmdlet yalnızca etiketleri güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="66ec9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66ec9-108">EXAMPLES</span></span>

### <span data-ttu-id="66ec9-109">Örnek 1: toplu Iş hesabındaki etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="66ec9-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="66ec9-110">Bu komut, pfuller adlı hesaptaki etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="66ec9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66ec9-111">PARAMETERS</span></span>

### <span data-ttu-id="66ec9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66ec9-112">-AccountName</span></span>
<span data-ttu-id="66ec9-113">Bu cmdlet 'in güncelleştirdiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-114">-Autostorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="66ec9-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="66ec9-115">Otomatik depolama için kullanılacak depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ec9-116">-DefaultProfile</span></span>
<span data-ttu-id="66ec9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66ec9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ec9-118">-ResourceGroupName</span></span>
<span data-ttu-id="66ec9-119">Bu cmdlet 'in güncelleştirdiği hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="66ec9-120">-Tag</span></span>
<span data-ttu-id="66ec9-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="66ec9-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66ec9-122">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="66ec9-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ec9-123">CommonParameters</span></span>
<span data-ttu-id="66ec9-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66ec9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ec9-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ec9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ec9-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66ec9-126">INPUTS</span></span>

### <span data-ttu-id="66ec9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="66ec9-127">System.String</span></span>

### <span data-ttu-id="66ec9-128">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="66ec9-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="66ec9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66ec9-129">OUTPUTS</span></span>

### <span data-ttu-id="66ec9-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66ec9-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="66ec9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66ec9-131">NOTES</span></span>

## <span data-ttu-id="66ec9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66ec9-132">RELATED LINKS</span></span>

[<span data-ttu-id="66ec9-133">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66ec9-133">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="66ec9-134">Yeni-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66ec9-134">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="66ec9-135">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="66ec9-135">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="66ec9-136">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="66ec9-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
