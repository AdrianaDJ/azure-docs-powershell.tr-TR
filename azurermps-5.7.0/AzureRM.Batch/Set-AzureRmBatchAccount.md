---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: 7f1747d838d0b81d1cfa29e98134897357f33a53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587683"
---
# <span data-ttu-id="0c1ec-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c1ec-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="0c1ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1ec-103">Bir toplu Iş hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c1ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c1ec-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c1ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="0c1ec-106">**Set-AzureRmBatchAccount** cmdlet 'ı bir Azure toplu hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="0c1ec-107">Şu anda bu cmdlet yalnızca etiketleri güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="0c1ec-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c1ec-108">EXAMPLES</span></span>

### <span data-ttu-id="0c1ec-109">Örnek 1: toplu Iş hesabındaki etiketleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0c1ec-109">Example 1: Update the tags on a Batch account</span></span>
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

<span data-ttu-id="0c1ec-110">Bu komut, pfuller adlı hesaptaki etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="0c1ec-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c1ec-111">PARAMETERS</span></span>

### <span data-ttu-id="0c1ec-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c1ec-112">-AccountName</span></span>
<span data-ttu-id="0c1ec-113">Bu cmdlet 'in güncelleştirdiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1ec-114">-Autostorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="0c1ec-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="0c1ec-115">Otomatik depolama için kullanılacak depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1ec-116">-DefaultProfile</span></span>
<span data-ttu-id="0c1ec-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1ec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c1ec-118">-ResourceGroupName</span></span>
<span data-ttu-id="0c1ec-119">Bu cmdlet 'in güncelleştirdiği hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1ec-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0c1ec-120">-Tag</span></span>
<span data-ttu-id="0c1ec-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c1ec-122">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0c1ec-122">For example:</span></span>

<span data-ttu-id="0c1ec-123">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="0c1ec-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1ec-124">CommonParameters</span></span>
<span data-ttu-id="0c1ec-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1ec-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1ec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1ec-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c1ec-127">INPUTS</span></span>

### <span data-ttu-id="0c1ec-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c1ec-128">None</span></span>
<span data-ttu-id="0c1ec-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0c1ec-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c1ec-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c1ec-130">OUTPUTS</span></span>

### <span data-ttu-id="0c1ec-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0c1ec-131">BatchAccountContext</span></span>

## <span data-ttu-id="0c1ec-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c1ec-132">NOTES</span></span>

## <span data-ttu-id="0c1ec-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c1ec-133">RELATED LINKS</span></span>

[<span data-ttu-id="0c1ec-134">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c1ec-134">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="0c1ec-135">Yeni-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c1ec-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="0c1ec-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0c1ec-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="0c1ec-137">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="0c1ec-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
