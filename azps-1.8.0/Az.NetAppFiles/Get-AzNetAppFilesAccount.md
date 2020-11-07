---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760785"
---
# <span data-ttu-id="401d2-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="401d2-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="401d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="401d2-102">SYNOPSIS</span></span>
<span data-ttu-id="401d2-103">Bir Azure NetApp dosyaları (ANF) hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="401d2-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="401d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="401d2-104">SYNTAX</span></span>

### <span data-ttu-id="401d2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="401d2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="401d2-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="401d2-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="401d2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="401d2-107">DESCRIPTION</span></span>
<span data-ttu-id="401d2-108">**Get-AzNetAppFilesAccount** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="401d2-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="401d2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="401d2-109">EXAMPLES</span></span>

### <span data-ttu-id="401d2-110">Örnek 1: ANF hesabı edinme</span><span class="sxs-lookup"><span data-stu-id="401d2-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="401d2-111">Bu komut, MyAnfAccount adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="401d2-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="401d2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="401d2-112">PARAMETERS</span></span>

### <span data-ttu-id="401d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401d2-113">-DefaultProfile</span></span>
<span data-ttu-id="401d2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="401d2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="401d2-115">-Name</span></span>
<span data-ttu-id="401d2-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="401d2-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="401d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="401d2-118">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="401d2-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d2-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="401d2-119">-ResourceId</span></span>
<span data-ttu-id="401d2-120">ANF hesabının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="401d2-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401d2-121">CommonParameters</span></span>
<span data-ttu-id="401d2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="401d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="401d2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="401d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401d2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="401d2-124">INPUTS</span></span>

### <span data-ttu-id="401d2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="401d2-125">System.String</span></span>

## <span data-ttu-id="401d2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="401d2-126">OUTPUTS</span></span>

### <span data-ttu-id="401d2-127">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="401d2-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="401d2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="401d2-128">NOTES</span></span>

## <span data-ttu-id="401d2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="401d2-129">RELATED LINKS</span></span>
