---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109178"
---
# <span data-ttu-id="3aa97-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3aa97-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="3aa97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aa97-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa97-103">Bir toplu Iş hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-103">Updates a Batch account.</span></span>

## <span data-ttu-id="3aa97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3aa97-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aa97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3aa97-105">DESCRIPTION</span></span>
<span data-ttu-id="3aa97-106">**Set-AzBatchAccount** cmdlet 'ı bir Azure toplu hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="3aa97-107">Şu anda bu cmdlet yalnızca etiketleri güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="3aa97-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3aa97-108">EXAMPLES</span></span>

### <span data-ttu-id="3aa97-109">Örnek 1: toplu Iş hesabındaki etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3aa97-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
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

<span data-ttu-id="3aa97-110">Bu komut, pfuller adlı hesaptaki etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="3aa97-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3aa97-111">PARAMETERS</span></span>

### <span data-ttu-id="3aa97-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3aa97-112">-AccountName</span></span>
<span data-ttu-id="3aa97-113">Bu cmdlet 'in güncelleştirdiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3aa97-114">-Autostorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="3aa97-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="3aa97-115">Otomatik depolama için kullanılacak depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="3aa97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa97-116">-DefaultProfile</span></span>
<span data-ttu-id="3aa97-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3aa97-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aa97-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa97-118">-ResourceGroupName</span></span>
<span data-ttu-id="3aa97-119">Bu cmdlet 'in güncelleştirdiği hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3aa97-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3aa97-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3aa97-120">-Tag</span></span>
<span data-ttu-id="3aa97-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="3aa97-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3aa97-122">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="3aa97-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3aa97-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa97-123">CommonParameters</span></span>
<span data-ttu-id="3aa97-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3aa97-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa97-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3aa97-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa97-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3aa97-126">INPUTS</span></span>

### <span data-ttu-id="3aa97-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3aa97-127">System.String</span></span>

### <span data-ttu-id="3aa97-128">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3aa97-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3aa97-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3aa97-129">OUTPUTS</span></span>

### <span data-ttu-id="3aa97-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3aa97-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3aa97-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3aa97-131">NOTES</span></span>

## <span data-ttu-id="3aa97-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3aa97-132">RELATED LINKS</span></span>

[<span data-ttu-id="3aa97-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3aa97-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="3aa97-134">Yeni-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3aa97-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="3aa97-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3aa97-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="3aa97-136">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="3aa97-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
