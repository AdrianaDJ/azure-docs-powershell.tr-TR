---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108963"
---
# <span data-ttu-id="35f39-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="35f39-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="35f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f39-102">SYNOPSIS</span></span>
<span data-ttu-id="35f39-103">Bir Azure NetApp dosyaları (ANF) hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="35f39-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="35f39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35f39-104">SYNTAX</span></span>

### <span data-ttu-id="35f39-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35f39-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35f39-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="35f39-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f39-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35f39-107">DESCRIPTION</span></span>
<span data-ttu-id="35f39-108">**Get-AzNetAppFilesAccount** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="35f39-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="35f39-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35f39-109">EXAMPLES</span></span>

### <span data-ttu-id="35f39-110">Örnek 1: ANF hesabı edinme</span><span class="sxs-lookup"><span data-stu-id="35f39-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="35f39-111">Bu komut, MyAnfAccount adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="35f39-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="35f39-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35f39-112">PARAMETERS</span></span>

### <span data-ttu-id="35f39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f39-113">-DefaultProfile</span></span>
<span data-ttu-id="35f39-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35f39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f39-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="35f39-115">-Name</span></span>
<span data-ttu-id="35f39-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="35f39-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f39-117">-ResourceGroupName</span></span>
<span data-ttu-id="35f39-118">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="35f39-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f39-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="35f39-119">-ResourceId</span></span>
<span data-ttu-id="35f39-120">ANF hesabının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="35f39-120">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f39-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f39-121">CommonParameters</span></span>
<span data-ttu-id="35f39-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35f39-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f39-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="35f39-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f39-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35f39-124">INPUTS</span></span>

### <span data-ttu-id="35f39-125">System. String</span><span class="sxs-lookup"><span data-stu-id="35f39-125">System.String</span></span>

## <span data-ttu-id="35f39-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35f39-126">OUTPUTS</span></span>

### <span data-ttu-id="35f39-127">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="35f39-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="35f39-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35f39-128">NOTES</span></span>

## <span data-ttu-id="35f39-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35f39-129">RELATED LINKS</span></span>
