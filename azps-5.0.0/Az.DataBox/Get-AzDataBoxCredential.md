---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321278"
---
# <span data-ttu-id="83006-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="83006-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="83006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83006-102">SYNOPSIS</span></span>
<span data-ttu-id="83006-103">Belirli bir işin databox kimlik bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="83006-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="83006-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83006-104">SYNTAX</span></span>

### <span data-ttu-id="83006-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83006-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83006-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="83006-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83006-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="83006-107">DESCRIPTION</span></span>
<span data-ttu-id="83006-108">**Get-AzDataBoxCredential** cmdlet 'i, belirli bir işin veri kutusunun kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="83006-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="83006-109">Döndürülen kimlik bilgileri nesnesinin iç özellikleri farklı SKU türleri için farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="83006-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="83006-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83006-110">EXAMPLES</span></span>

### <span data-ttu-id="83006-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="83006-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="83006-112">Bu, belirtilen işin iş sırlarını yeniden tunlar</span><span class="sxs-lookup"><span data-stu-id="83006-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="83006-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="83006-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="83006-114">Bu, belirtilen işin iş sırlarını yeniden tunlar</span><span class="sxs-lookup"><span data-stu-id="83006-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="83006-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83006-115">PARAMETERS</span></span>

### <span data-ttu-id="83006-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83006-116">-DefaultProfile</span></span>
<span data-ttu-id="83006-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83006-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83006-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="83006-118">-Name</span></span>
<span data-ttu-id="83006-119">Databox Iş adı</span><span class="sxs-lookup"><span data-stu-id="83006-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83006-120">-ResourceGroupName</span></span>
<span data-ttu-id="83006-121">Databox Iş kaynağı grubu adı</span><span class="sxs-lookup"><span data-stu-id="83006-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="83006-122">-ResourceId</span></span>
<span data-ttu-id="83006-123">Databox Iş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="83006-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83006-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83006-124">CommonParameters</span></span>
<span data-ttu-id="83006-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83006-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83006-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83006-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83006-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83006-127">INPUTS</span></span>

### <span data-ttu-id="83006-128">System. String</span><span class="sxs-lookup"><span data-stu-id="83006-128">System.String</span></span>

## <span data-ttu-id="83006-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83006-129">OUTPUTS</span></span>

### <span data-ttu-id="83006-130">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. modeller. UnencryptedCredentials, Microsoft. Azure.,. DataBox, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="83006-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="83006-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83006-131">NOTES</span></span>

## <span data-ttu-id="83006-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83006-132">RELATED LINKS</span></span>
