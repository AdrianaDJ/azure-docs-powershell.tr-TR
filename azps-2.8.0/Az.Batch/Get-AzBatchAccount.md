---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 48080fde4c7187bcbcf601cb136373cc16ef7503
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938654"
---
# <span data-ttu-id="cffcf-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cffcf-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="cffcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cffcf-102">SYNOPSIS</span></span>
<span data-ttu-id="cffcf-103">Geçerli abonelikte bir toplu Iş hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="cffcf-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="cffcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cffcf-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cffcf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cffcf-105">DESCRIPTION</span></span>
<span data-ttu-id="cffcf-106">**Get-AzBatchAccount** cmdlet 'i geçerli abonelikte bir Azure toplu hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="cffcf-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="cffcf-107">*AccountName* parametresini tek bir hesap almak için kullanabilir veya bu kaynak grubu altında hesapları almak Için *resourcegroupname* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cffcf-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="cffcf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cffcf-108">EXAMPLES</span></span>

### <span data-ttu-id="cffcf-109">Örnek 1: ada göre bir toplu hesap alma</span><span class="sxs-lookup"><span data-stu-id="cffcf-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="cffcf-110">Bu komut, pfuller adındaki toplu iş hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="cffcf-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="cffcf-111">Örnek 2: kaynak grubuyla ilişkili toplu hesapları alma</span><span class="sxs-lookup"><span data-stu-id="cffcf-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="cffcf-112">Bu komut, CmdletExampleRG kaynak grubuyla ilişkili toplu iş hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="cffcf-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="cffcf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cffcf-113">PARAMETERS</span></span>

### <span data-ttu-id="cffcf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cffcf-114">-AccountName</span></span>
<span data-ttu-id="cffcf-115">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cffcf-115">Specifies the name of an account.</span></span>
<span data-ttu-id="cffcf-116">Bir hesap adı belirtirseniz, bu cmdlet yalnızca bu hesabı döndürür.</span><span class="sxs-lookup"><span data-stu-id="cffcf-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffcf-117">-DefaultProfile</span></span>
<span data-ttu-id="cffcf-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cffcf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cffcf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffcf-119">-ResourceGroupName</span></span>
<span data-ttu-id="cffcf-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cffcf-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cffcf-121">Bir kaynak grubu belirtirseniz, bu cmdlet belirtilen kaynak grubu altındaki hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="cffcf-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cffcf-122">-Tag</span></span>
<span data-ttu-id="cffcf-123">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="cffcf-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cffcf-124">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"} Bu cmdlet, bu parametrenin belirttiği etiketleri içeren hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="cffcf-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffcf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffcf-125">CommonParameters</span></span>
<span data-ttu-id="cffcf-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cffcf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffcf-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cffcf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffcf-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cffcf-128">INPUTS</span></span>

### <span data-ttu-id="cffcf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cffcf-129">System.String</span></span>

### <span data-ttu-id="cffcf-130">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cffcf-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cffcf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cffcf-131">OUTPUTS</span></span>

### <span data-ttu-id="cffcf-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cffcf-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cffcf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cffcf-133">NOTES</span></span>

## <span data-ttu-id="cffcf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cffcf-134">RELATED LINKS</span></span>

[<span data-ttu-id="cffcf-135">Yeni-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cffcf-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="cffcf-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cffcf-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="cffcf-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="cffcf-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="cffcf-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="cffcf-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
